# WebGPU :: Javascript at the speed of Light 

This is the FAQ Readme file for the video down below.

**Corrections of mistakes in the video is pinned in the comments section of the video.**

## https://youtu.be/oAwlk0j5RUM
[![WebGPU Compute Shaders Introduction](https://github.com/visionary-3d/webgpu-faq/assets/64514807/eb3b86ce-5f24-4a3a-a03c-e7aad86cf6c5)](https://youtu.be/oAwlk0j5RUM)

## FAQ

### Where does WebGPU code even run?
Images are always better than words:
![image](https://github.com/visionary-3d/webgpu-faq/assets/64514807/ddfba62f-856b-43be-820d-1d7a04711756)

[Capturing the WebGPU ecosystem Article](https://developer.chrome.com/blog/webgpu-ecosystem/)

### How am I measuring gpu compute time ?
I'm using a special flag in chrome which allows me to use some timer tools:

```--enable-dawn-features=allow_unsafe_apis```

You can learn more about how to use this flag here:
[GPU Timer Tool For WebGPU](
https://matrix.to/#/!MFogdGJfnZLrDmgkBN:matrix.org/$D342y3gRpy3EndUMK1nzbL7Qwvn6wozusB6wCROTuZs?via=matrix.org&via=mozilla.org&via=matrix.nrp-nautilus.io)

### Can WebGPU be used for native mobile or desktop apps?
Yes. You can write C++ or Rust code to create native applications with WebGPU.
However support for some browsers and specially mobile browsers is Work In Progress at the moment.

### What exactly are the advantages of WebGPU vs ThreeJS + WebGL ? 

1. Biggest one in my opinion is compute shaders. Compute shaders allow you to run you shader in parallel on the gpu but they're way more flexible and more general purposed than VS and FS shaders.
Before, you could do what you can do in compute shaders in normal Fragment shaders, but that was much more difficult to do. So ease of use is a key factor.

2. WegGL is an ugly mess. WebGPU is a fantastic upgrade and has a way simpler API.

3. WebGPU is built on top of Vulkan ( for windows ) and Metal ( for mac ) I beleive.
Vulkan has some really nice features for Raytracing as far as I'm aware of and so, we're going to have a RayTracingPipeline further down the line.

### How much easier would it be to start with the framework like Babylon.js instead of trying to understand the WebGPU ?
It's not that different at the moment. And I highly recommend learning WebGPU itself.
