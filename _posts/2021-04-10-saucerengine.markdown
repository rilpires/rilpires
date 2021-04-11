---
layout: post
title: Saucer Engine
---

Saucer engine is a Open Source 2D Game engine I made during 2 months with C++/OpenGL/GLFW/etc. There is a builtin editor and support for Lua scripting. The name *Saucer* came simply from my name ("Pires" literally means Saucer) <span class="smoll">, but it came together with the proposal to "be lightweight" hum? *ba dum tsss*</span>

<br>
<img style="width:90%" src="/assets/images/saucer_preview.png">
<br>
<br>
<a href="https://github.com/rilpires/saucer_engine"><img src="/assets/images/github.png" style="height:32px">Github Page</a>
<br>

<h1 class="title">Development</h1>
Ohhh the naive old me...

<br>

The plan was to make a *"simple retro-like Chess game"* (motivated by the popular Netflix show with the pretty girl you know about). But I also always had wanted to learn low-level graphics stuff with C++... so it was settled: I would create this chess game with a game engine I made myself.

Fast forward: I made it!!! <a href="https://rilpires.itch.io/1bchess">Here is the page on itch.io</a>. Even though my first expectations was to complete everything in 1 month (naive old me!!!), now I don't think 2 months was too much. Important note: My objective wasn't to complete only the *"simple retro-like Chess game"*. This was postponed until the engine was "complete", and this one was the task that took 95% of the time. I was a little further than my first concepts of what was a "complete" engine, and still, even then now I see that it is not complete.

<br>
Feature-wise, I'm pretty satisfied with the result:
<ul style="text-align:left">
    <li>
        Texture(PNG) and custom font(TTF) rendering, with support to write own GLSL shaders.
    </li> <li>
        Audio sample(WAV) & stream(OGG) player.
    </li> <li>
        Embedded Lua scripting & runtime profiling.
    </li> <li>
        Physics engine (<a href="https://box2d.org/">Box2D</a>) integrated
    </li> <li>
        Assets packaging for release build (Using zlib)
    </li> <li>
        `Scene` objects are saved as git-friendly YAML files.
    </li> <li>
        Very lightweight (release export is around 4MB, aside assets).
    </li> <li>
        Builtin editor for scene editing (There is no way I'd have decided to make it without <a href="https://github.com/ocornut/imgui">ImGui</a>)
    </li>
</ul>

<br>
If I ever want to create another 2D simple game or maybe some general application with graphics, I'd even reuse it again. But, to be honest, it was TOO²³²³³ much work for something you could achieve with other tools.

<br>
Now, I'm not saying I regret doing it. I learned a lot about C++ development and stuffs I was targeting to learn. These C++ metaprogramming templates Hell ? Scare me no more. Macros can be useful with the right amount of care taken. And in the end of the day I can think of many ways to optimize this code but hey, I don't even need it because C++ is lighting speedy boy.

<br>
<img alt="Benjamin Franklin: 'Those who gave up performance for easiness deserve neither'" style="height:300px" src="/assets/images/benjaminfranklin.jpg">
<img style="height:300px" src="/assets/images/templatemacrohell.png">
<br>

<br>
<h1 class="title">Documentation</h1>
Simply put: there isn't any.

<br>
Sorry mom. It was already too much of unpaid work to I even think about documentating it for other users. Tried Doxygen but ehh... I decided I should expose the Lua API instead the C++. That's why I'm saying the engine is "complete", with the quotation mark.

<br>
<img alt="Mr. Turner: 'This is where I'd put my documentation if I had one" style = "height:500px" src ="/assets/images/mydoc.png">
<br>

<br>
<h1 class="title">Building</h1>

<h2>Figure it yourself, good luck.</h2>

<br>
Just kidding. This was probably one of the most painful tasks. Until I had to move to Windows from Linux, it was all a customized Makefile. It was nothing fantastic but did the job. Unfortunately, Windows doesn't simply builds from a Makefile. So I took some time to learn CMake.

<br>
<img alt="Sad girl at computer" style="height:300px" src="/assets/images/sadcomputer.gif">
<br>

<br>
There is a CMake file. I pray that you can simply build it. As I'm writing this page, it works on Windows VSCode + MSVC 2019 with the famous CMake plugin out there.

<br>
I very appreciate the effort of the CMake team. To be honest, I don't even know if it could be easier. But there isn't a single one easy `Getting started` tutorial. All the good efforts out there from outside the official documentation doesn't cover everything you will need to know. And the official docs is just TOO much, when all you want is some simple steps. My conclusion is that if I ever had to hire a team of at least 3 C++ programmers, I'd hire someone entirely dedicated to compile & link stuffs.

<br>
<h1 class="title">Conclusions</h1>
<ul style="text-align:left">
    <li>
        C++ is just the right amount of hard and unlimited amount of power.
    </li><li>
        You can do bollocks and C++ will still be faster than other solutions.
    </li><li>
        Making games with C++ is a totally different task from making a general-purpose game engine.
    </li><li>
        Embedding Lua was way easier than expected. I just don't like it's syntax!! But it still is a very useful tool.
    </li><li>
        You gotta be prepared to learn things you were not expecting to, like, in my case, the bare minimum of audio programming. It isn't just "play me this file please" you know... still, kinda satisfying knowledge.
    </li><li>
        Even though there isn't any documentation, I'm pretty happy with how things came together at the end. The assets packaging, the last feature I made, was surprisingly satisfying. It isn't in any way hack-proof, but I convinced myself that barely no game out there is?
    </li><li>
        In the end, I wasn't any motivated to play a single game of Chess (!!!). More on that in another post maybe.
    </li>
</ul>

<br>
<h2 class="title">Acknowledgments</h2>
<ul style="text-align:left">
    <li>
    <a href="https://learnopengl.com/"> LearnOpenGL</a> 
    </li>
    <li>
        Aside from OpenGL, every other integrated library has a proper documentation when necessary. Check them on the <a href="https://github.com/rilpires/saucer_engine#dependencies">Github Page</a>
    </li>
</ul>