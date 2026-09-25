# Node.js starter

[![Deploy on velixir](https://velixir.net/img/deploy-on-velixir.svg)](https://velixir.net/new?template=node-http)

The smallest thing that can be called a Node service: the built-in `http` module, no
framework, nothing to install.

[Deploy it on velixir](https://velixir.net/new?template=node-http) and you get a live URL in
under a minute.

## Running it locally

```bash
node index.js
```

Then open http://localhost:8080.

## Deploying

velixir builds your source server-side, so there is no Dockerfile to write and nothing to
build on your machine.

```bash
velixir deploy
```

## The one rule

Bind `process.env.PORT` on `0.0.0.0`. velixir injects `PORT` and routes the edge to it;
a container that hardcodes a port, or binds `localhost`, builds fine and then never passes
a health check.

## Licence

MIT.
