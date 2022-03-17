# Oct 4th, 2021

Started working on a prototype of a terminal emulator, the first part is to get a window opened
and render stuff on its surface. With the help of `wgpu` and `wgpu_glyph`, it's a piece of cake.

The problem is when I started a `pty` pair, the whole application choke because I tried to read from
`ptm` right in the event loop. Can't handle it differently because I don't have a proper
architecture.

# Where it begins

Was building a JS playground to help visualize how variables change during execution. It requires user to manually write log using `debug()` method.

Would be great if the app can automatically detect changes or print out everything needed to see at each step, just like a debugger.

To achieve this, I need to write a debugger that run inside the browser. This is doable but the amount of works is just absurb. It include a complete rewrite (or reinvent) of a JavaScript engine, which doesn't seems so productive at all. I need to find another approach to do it.

Then I discovered the Chrome Debugging Protocol, which is exactly what I needed. It's the communication protocol to let you communicate with a running Node.JS Debugger or Chrome Debugger process, control the debug flow such as step in, step out, execute code on the current call frame,...

# The PoC

I quickly came up with a small PoC that run inside a terminal, the way it work is: Take a code snippet, write it to a temporary folder, spawn a new `node` process with `--inspect-brk` parameter to put it in debugging mode, then connect to it via a library called `chrome-remote-interface`, it can do some debugging command like step in, step out,...

This PoC helped me understand the protocol better and able to figure out what I could build from it.

At the very beginning, I had to deal with a poorly documented protocol with lots of hidden behavior, takes a lot of time to figure out what's going on and how to get over them.

For example, calling `Debugger.pause` doesn't immediatelly pause the debugger, but the method has a callback so it seems confusing, I thought we can handle the pause event in that callback. Turned out, we need to handle `Debugger.paused` event in order to do so.

Stuff like `Debugger.stepIn` also need to be executed when the debugger is paused.

So I scoped out what's the next version look like:

- A small debugger that can execute any code snipped input from the user
- The call stack is limited to the scope of current code, that mean, all call frames that belongs to Node.js internal will be step over.
- There will be a watch list where you can see the values on current call frame.

# 03.18.2022 - Test my site/Markdown render

## LOL :v
