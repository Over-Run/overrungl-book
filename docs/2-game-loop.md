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

This is just a simple example. We must use a **Timer** to calculate the interval (called _delta_) of the last and current
running time.

We can use a simple timer. It computes the delta, so we can use it for the scaling factor.

```c
double lastTime, currentTime, delta;
while (running) {
    lastTime = currentTime;
    currentTime = getCurrentTime();
    delta = currentTime - lastTime;
    update();
    render();
    post_processing();
}
```


