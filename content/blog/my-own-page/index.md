+++
title = 'How I created my own page'
description = "Some days ago, I was constantly asked if I had any website. Every time I replied with no, it filled me with sadness. Therefore I created this website to stop the haters! But how should I desing my very own page? Which content should I put into it? What do I want, or sometimes more important, don't want?"
date = 2026-03-28
+++

Some days ago, I was constantly asked if I had any website. Every time I replied with no, it filled me with sadness. Therefore I created this website to stop the haters! But how should I desing my very own page? Which content should I put into it? What do I want, or sometimes more important, don't want?

## My Plan

My plan was simple: I don't really have a plan, so let's just try things out!

- I wanted a minimal design wich focuses on readability. I thought for a second to make every text red/green, so that my dad couldn't read it, only then to realize that he will not find this page in the first place.
- No JS/TS/Tailwind CSS. Generally nothing that contains NPM, adds a dependency or any fancy web framework. I still ended up using hugo for statically generating the html files.
- No WASM or Rust code for basic web elements. *(Yes, I am talking to [you](https://lovirent.eu/)!)*
- I wanted to host all games that I created with others during the Questpresso gamejams.
- I wanted to create a blog. My current plan for the blog is that I don't have a plan! I will start posting the most random things about pretty much everything.
- Maybe I create a page about all my finished and upcoming projects, that are somehow relevant. I am still figuring out which project is relevant enough to deserve its own page and which project is just a sandbox-try-it-out-and-fail-fast-idea

## Getting Started

I first set up Nix, Hugo and Pandoc. I needed Nix for managing the (hopefully few) dependencies. Hugo was required for generating the html pages based on layouts and markdown content. Personally, I prefer the pandoc extensions for compiling the Markdown files. Pandoc for example supports footnotes and callouts.

```sh
nix-shell -p hugo pandoc
```

But then I quickly found out that the hugo support for pandoc was ... meh. You can not easily pass cli args to the binary and instead need to setup a shell file for the new pandoc, add it to the path and run this instead.

I love rainbows! Therefore I wanted to put a rainbow effect on every top level header.

```css
h1 {
  font-size: 3rem;
  text-transform: uppercase;
  color: #ff5722;
  text-shadow: -4px 4px #ef3550,
               -8px 8px #f48fb1,
              -12px 12px #7e57c2,
              -16px 16px #2196f3,
              -20px 20px #26c6da,
              -24px 24px #43a047,
              -28px 28px #eeff41,
              -32px 32px #f9a825;
}
```
