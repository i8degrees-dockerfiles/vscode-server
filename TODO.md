
# vscode-server

## TODO

- [ ] figure out the `Dockerfile` reference syntax
for letting us use the `command` syntax inside of 
`compose.yml` services along side a sane default 
entrypoint. I believe it has something to do with
maybe the `CMD` syntax inside `Dockerfile`..?

- [ ] determine if we need to run `code serve-web` or `code tunnel` or even
both? shall we do so in two separate containers?

- [ ] register **vscode.fs1.home**

- [ ] try out the `debian:12.10-slim` image
  * This drops the file size from ~`50 MB` to
  ~`30 MB`; this could improve initial setup cost
  ever so slightly, but at what cost? What is being
  dropped from the larger image???
