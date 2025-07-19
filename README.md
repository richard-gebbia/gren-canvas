# gren-canvas

This is a proposal on how to build an HTML canvas API for [Gren](https://gren-lang.org).

The way this PoC works is that, each update tick, it pushes a series of commands to a port. On the JS side, these commands are parsed and executed on a target canvas.

The ideal API would do this transparently, interpreting the output of `view` to execute these commands, so no `Cmd`s are needed.

## Plan
- [ ] Dynamically interpret `CanvasRenderingContext2D` calls from Gren
- [ ] `clearRect`
- [ ] `fillStyle`
- [ ] `fillRect`