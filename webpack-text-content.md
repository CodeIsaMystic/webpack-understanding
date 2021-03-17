<div align="center">

<a href="https://webpack.js.org/">
  <img
    height="60"
    width="240"
    alt="webpack-logo"
    src="assets/icons/webpack-icon.png"
  />
</a>

<h1>WebPack</h1>



Really when you think about where we came from to why we're trying to do these things are all about performance and being able to scale it, being able to maintain it.
Anf having this module system, especially ESM, has really transformed the opportunities that are possible with bundlers.
And there is no other syntax that is as unique as the ES Module spec, so much so that it is now being adopted by other programming languages.
C++ has RFCs right now to consider adopting this module syntax, because it's so profound and so powerful for stack analysis.
You think back to, I worked on objective C, so I think of, you gotta include a bunch of headers and you just include crap.
And you don't care, like how much it costs you, but we don't have that luxury in the web, right? 
We have to care how much code we're compiling and shipping.
And so even the WebAssembly specification is now modeled exactly, alomst identically in the same way from the ES Module spec.
So, I don't know why Rust decided to do their own thing, but ...


And it depends on nav.js and footer, at least I think we stop at 20 modules or something like that.

You can see a very clear graph of here's your entry point.

"It has a dependency on index.js,which is your entry point itself."

And so you're kind of seeing there's a graph that's being built here, and we call this the dependency graph in webpack.
You want to have everything that's, anything that you access from another file we can run so like, node ./dist/main.js.
We get all the strings there, right??

you want to have everything that's, anything that you access form another file 

like, in modules, you don't want to have side effects, right?
you want to have everything that's, anything that you access form another file 
should just be trough exports or a default export.
Instead of just like, running a script and 
evaluating what kinds of things are hapenning inside of it.
Now we have some rules in Webpack that just say, you cannot use CommonJS and ES syntax in the same file.
I would throw an error.
Or you can't use an export, and then a default exports, or a module.exports.
So what I tend to do is usually just use the ESM syntax at the top level.
Webpack supports using require, but what we'll do is we actually have interrupt to support using both and have it work accurately with the correct cyclical dependencies and light binding.
So since qe know this is a default export, we can actualy call this like,
...
