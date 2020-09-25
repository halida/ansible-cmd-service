# ansible-cmd-service

Systemd user level service for one command.

## Usage

Clone to your roles folder as `cmd-service`, then in your playbooks file:

```yaml
  import_role:
    name: cmd-service
  vars:
      name: 'python-http-server'
      path: '/tmp/http_shared'
      cmd: "/usr/bin/python -m SimpleHTTPServer 8888 "
```

Start service:

```sh
systemctl --user start python-http-server
```
