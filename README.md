# stop-server [![](https://badge.fury.io/js/stop-server.svg)](https://www.npmjs.com/package/stop-server) [![](https://travis-ci.org/typicode/stop-server.svg?branch=master)](https://travis-ci.org/typicode/stop-server)

> Shut down :zap: your computer with your phone and a browser (works on OS X, Linux and Windows)

_Created because I usually watch movies on my computer from my bed and I wanted to be able to shut it down remotely :)_

## Usage

1. Install `stop-server`

  ```bash
  npm install -g stop-server
  stop-server start # Need to be done only once
  ```

2. Visit [http://localhost:5709/qr.html](http://localhost:5709/qr.html) on your computer and scan the QR code or go directly to `http://your-local-ip:5709` __on your phone/tablet__. You should see this page:

  ![](http://i.imgur.com/lWW1LTE.png)

3. That's all :)

__Important__ on __OS X__ and __Linux__ you need to allow the `poweroff` command to be used without admin password:

```bash
# Run 'sudo visudo' and add
your-username ALL=NOPASSWD: /sbin/poweroff
```

## Uninstall

```
npm rm -g stop-server
```

## How it works?

stop-server is a simple Express server. When you call `DELETE http://your-local-ip:5709`, it runs `poweroff` (OS X, Linux) or `shutdown` (Windows).

stop-server is automatically started on log in using [user-startup](https://github.com/typicode/user-startup).

## License

MIT - [typicode](https://github.com/typicode/stop-server)
