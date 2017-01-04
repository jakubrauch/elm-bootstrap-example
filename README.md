# elm-bootstrap-example

A Task List implemented with Elm enriched with Bootstrap styling (no Bootstrap JS).

In general, Task List is a perfect case for getting started with a new UI language. It requires the
page to be interactive, update its state but also remains fairly simple and its goal
is straightforward for everyone.

This particular implementation does not involve any backend systems or storage. There are
 no submodules nor additional functions. All to keep the source code clear for the newcomers,
 yet something that shows a popular frontend framework in use.
 This is just plain Elm code with some Bootstrap formatting to show how a typical 
 Task List case translates to an Elm reality.
 
## Start

Install elm (https://guide.elm-lang.org/install.html), clone this repo, navigate to 
the project folder (elm-bootstrap-example) and run:

```
elm-reactor
```

This will start up a server and expose your project files via browser:

```
elm-reactor 0.18.0
Listening on http://localhost:8000`
```

Go to your browser and navigate to http://localhost:8000/Hello.elm. It will compile your code and
will present the Task List.

## Structure
 
Application has three files:
 - Hello.elm - Elm implementation of the Task List web page (incl. Bootstrap styles)
 - elm-package.json - Configuration of dependencies for the project
 - style.css - CSS styling not covered by Bootstrap

## First Step - Elm logic

The first step I took was implementing a plain Task List without any Bootstrap additions - I wanted to
have logic working well before styling the page. There are two very useful resources for getting started
with Elm:
 - https://guide.elm-lang.org
 - https://www.elm-tutorial.org/en/
 
Description of the actual logic of the webpage is located in comments inside Hello.elm file.

### Second step - Bootstrap

I looked around the web and found some attempts to add Bootstrap functionality to the Elm application as a
module. There are a couple of options:

http://package.elm-lang.org/packages/circuithub/elm-bootstrap-html/latest
https://github.com/pzavolinsky/elm-bootstrap

However, I was looking for a more generic approach where I could just use plain bootstrap styling, without it being
hidden behind some additional library yet I did not need to use the fancy JavaScript tools it provides. 
I also prefer to have the latest bootstrap version available at a hand. Then I stumbled 
upon this article:

https://bendyworks.com/blog/elm-frontend-right-now-updated-for-0-18

There we have a much more advanced Task List application by Brad Grzesiak and he uses some custom made Bootstrap
references. This convinced me to stick with the basic approach and reference Bootstrap's styling manually. As long as 
it is not much work in Elm I prefer to keep it as basic as possible.



### Third step - Final styling

The final styling of the components has been located in style.css. I have added only a few 
custom classes to the Hello.elm file and tried to keep entire custom styling limited to the
style.css file.


## Utilities
Here are some useful tools for Elm apps:
 - IntelliJ elm-plugin - http://durkiewicz.github.io/elm-plugin
 - elm-format - https://github.com/avh4/elm-format
   - IntelliJ support - https://github.com/durkiewicz/elm-plugin/issues/9

## Impressions

### First Impressions - Elm logic
Well, I am amazed by Elm. Soon after starting coding I was already able to synchronize webpage model state with input 
form field. While this was not a one-liner it was fun to write because any issues were clearly reported
to me by the compiler. Once this part was written I suddenly realized that I am almost done implementing entire
logic. The only thing missing in my app was just to add this text to a list of entries in the model. This part
went even quicker than I thought - the page was ready in no time. 

No testing, debugging, checking edge cases, just reacting to compiler's suggestions. I used to code in OCaml
 but it did not give me the same confidence as Elm does. I know a bit of Haskell and Elm resembles Haskell a lot with
 its syntax which I like. However, I find Elm much more modern and user-friendly than its 26-old ancestor. I am
 looking forward to getting to know it.
 
### Second Impression - Bootstrap

If you know Bootstrap then adding it to the Elm's Html hierarchy is very straightforward and the Elm Html tags
translate directly to corresponding plain Html tags. Not much more to add here, except that Bootstrap JS is not
simple to integrate. Elm introduces its own apprach to interoperability with existing JavaScript library and I have
not found an Elm module that has a complete set of Bootstrap features covered.

### Third Impression - Final styling

The last step was adding some finishing touches to the layouts. This meant writing some CSS
class definitions and surprisingly it was the toughest part for me. My CSS knowledge may have
become a bit rusty over last year but I did not expect to find it that intimidating.
For me it was like driving off
a freshly opened tarmac highway to a wet, muddy, unpaved dirt. Every little thing suddenly started to take way more 
time than it would expect it to take. Some heights not calculated, some aligns not working, 
some blocks not acting as blocks. Nothing was like in the pure world of functional Elm.  

This somewhat concludes my overall impression of the UI reality of past decade... The gap between Elm and CSS showed
me how different this new functional UI language is from the other, older UI technologies. My opinion
may be biased towards Elm because I do like functional languages and I do like Haskell (which Elm resembles) so 
I would like to encourage you to try it out yourself and share your impressions.