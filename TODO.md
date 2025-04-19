
# vscode-server

## TODO

- [x] figure out the `Dockerfile` reference syntax
for letting us use the `command` syntax inside of 
`compose.yml` services along side a sane default 
entrypoint. I believe it has something to do with

- [x] determine if we need to run `code serve-web` or `code tunnel` or even
both? shall we do so in two separate containers?

- [ ] register a couple subdomains of scorio.home in our auth DNS. This is
for my own convenience for quickly remembering where our tunnel and web UI
is. I would like to dynamically register it upon starting the service 
followed by using nginx or such to transparently proxy each subdomain to its
destination so that we do not have to use or remember adding `:<port>` at the
end of every URI.
  * vscode-web.scorpio.home
  * vscode-tunnel.scorpio.home

- [ ] investigate how to set vscode-web up with a self-signed certificate from
our PKI; we can then modify the container port to 443.

- [ ] try out the `debian:12.10-slim` image
  * This drops the file size from ~`50 MB` to
  ~`30 MB`; this could improve initial setup cost
  ever so slightly, but at what cost? What is being
  dropped from the larger image???
