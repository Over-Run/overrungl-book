# Preparing

Before staring, we need to prepare our project. We will use Java 19 for our project.

Add the dependency to your build script. In the future, we can use the customizer.

```groovy
// Groovy
dependencies {
    implementation "io.github.over-run:overrungl:0.1.0"
    implementation "io.github.over-run:overrungl-glfw:0.1.0"
    implementation "io.github.over-run:overrungl-opengl:0.1.0"
    implementation "io.github.over-run:overrungl-stb:0.1.0"
    implementation "io.github.over-run:overrungl-glfw::natives-windows"
    implementation "io.github.over-run:overrungl-stb::natives-windows"
}
```

If you had used LWJGL before, you may see that the there is no native for core and OpenGL module.
This because the OpenGL module used core and GLFW module to load functions,
and we don't have to build shared libraries for it.

To get started with OverrunGL, we use [this example](https://github.com/Over-Run/overrungl/wiki/Getting-Started).
You can see we are using GLFW for our window, so we can interact with mouse, keyboard even controllers.

If all works, you will get a red window like this below.

![Window with red background](img/1-red-window.png)
