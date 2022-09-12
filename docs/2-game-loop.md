# The Game Loop

In this chapter, we will create a game loop for our game engine. The game loop is the core in our engine. It updates the
framebuffer, processes the input and display to the screen, until the game engine exits.

This pseudocode shows the basic logic of the game loop.

```c
while (running) {
    update();
    render();
    post_processing();
}
```

But it is not all. We must set the limit for the running time. If it runs too fast or slow,
we can't fully interact with the engine.
