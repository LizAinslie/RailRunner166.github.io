---
layout: post
title: "Elixir - The Best Dev Language"
summary: I've been learning a new programming language!
featured-img: nick-karvounis-402158
categories: [Programming]
---

Recently, I've been learning a new programming language, Elixir. Elixir is a readable extension of the Erlang <abbr title="Virtual Machine">VM</abbr>.

I am already writing a library that attempts to do in Elixir what [Lodash](https://lodash.com/) does in JavaScript. I call it Hidash, lol.

Some example Elixir code goes as follows:

```elixir
avg = fn a, b -> (a + b) / 2 end

IO.puts("The average of 3 and 7 is #{avg.(3, 7)}")

# Output: The average of 3 and 7 is 5.0
```

I plan on adding a more advanced `average` function to the `HiDash.Math` module soon.

Ruby supports bare words after a function `method_missing` is defined, but Elixir supports them by default. I don't use them, because that's insane, but it's a cool feature to have ~~and to play around with~~.

I plan on making my second Discord bot using Elixir, but before that, I need to get some practice. I plan on open-sourcing all my projects, so check out [my GitHub](https://github.com/RailRunner16?utf8=%E2%9C%93&tab=repositories&q=&type=&language=elixir)
