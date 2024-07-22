+++
title = "gpuplay"
date = 2024-05-04
extra.link = "https://github.com/atadier/gpuplay"
+++

A small command line application to visualize GPU shaders built with the `wgpu` graphics API.

<!-- more -->
I built a small GPU shader visualization tool as a first hands-on endeavour in the world of Rust graphics and hardware acceleration.

{{ img(path="img/gpuplay.png", alt="Screenshot of the gpuplay application") }}

The simplicity of this project demonstrates quite well the power of using [`wgpu`](https://github.com/gfx-rs/wgpu/) as a graphics abstraction: the application can make use of different graphics APIs to target all platforms with a relatively small codebase. I would even imagine that it would have taken me more time to write this application only targeting one of the low level APIs like Vulkan.

Another library I made use of is [`naga`](https://github.com/gfx-rs/wgpu/tree/trunk/naga), a shader translation facility integrated in `wgpu` that made it easy to add support for shading languages like [WGSL](https://gpuweb.github.io/gpuweb/wgsl/) as well as [GLSL](https://github.com/KhronosGroup/glslang) without worrying too much about their differences. I found that it is also a useful tool to learn more about shading languages in general since it also has a [CLI](https://crates.io/crates/naga-cli) to convert shaders from one language to the other, which helped me compare the syntax of the two languages quickly.

I'm happy to see that the `wgpu` project is becoming the de-facto library for hardware-accelerated graphics in Rust as there are clear benefits to having readily available cross-platform graphics infrastructure. It also has a lot of significance to me as it was [the first open-source project I contributed to](https://github.com/gfx-rs/wgpu/pull/2801), just two years ago at the age of 16. The maintainers helpfully welcomed my naive contribution, and I ended up using the API that I had introduced back then into this new project.
