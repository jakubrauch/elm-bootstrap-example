# elm-bootstrap-example

Work in progress - created a simple todo-list - no bootstrap added yet.

## First step - create a task list:

By the time I was finished writing code that would reflect in the model all input field changes I suddenly realized that
 the only thing missing in my app is addition this text to a list - a trivial job!
 Everything else is already implemented and verified by the compiler.
  
If you ever liked working with enums in Java because they gave you the confidence of what are the possible
 values - you will love Elm for being very explicit. I had some doubts in what others said about Elm - that you get all
  the issues on compilation time. I also doubted in clarity of the compiler messages. I... was wrong.
  I used to code in OCaml, tried a bit of Haskell, but they did not give me the same feeling of confidence in the
   correctness of the code as Elm does.
 
## Second step - wire up Bootstrap:

I looked around the web and found some attempts to add Bootstrap functionality to the Elm application. There are
a couple of options:
http://package.elm-lang.org/packages/circuithub/elm-bootstrap-html/latest
https://github.com/pzavolinsky/elm-bootstrap

However, I was looking for a more generic approach where I could just use plain bootstrap styling, without the fancy
JavaScript tools it provides. I also prefer to have the latest bootstrap version available at a hand. Then I stumbled 
upon this article:
https://bendyworks.com/blog/elm-frontend-right-now-updated-for-0-18

Here we have a much more advanced todo list application by Brad Grzesiak and he uses some custom made bootstrap
references. This convinced me to stick with the basic approach and reference bootstrap's styling manually. As long as 
it is not much work in Elm I prefer to keep it as basic as possible.