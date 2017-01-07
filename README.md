# elm-bootstrap-example

A Task List implemented in Elm with Bootstrap styling (without Bootstrap JavaScript components).

The functionality is very simple - an in-memory Task List with options to add and remove unique entries.
The code is very basic - there are no submodules or additional functions. The purpose is 
to make the source code straightforward for the Elm newcomers. 
 
## Start

Install Elm (follow: https://guide.elm-lang.org/install.html) and clone this repo:
```
git clone git https://github.com/jakubrauch/elm-bootstrap-example.git
```
Navigate to the project folder (where TaskList.elm file is located) and run:

```
elm-reactor
```

This will start up a server and expose your project files via a browser:

```
elm-reactor 0.18.0
Listening on http://localhost:8000`
```

Go to your browser and navigate to http://localhost:8000/Hello.elm. It will compile your code and
present the Task List that you can modify.

## Structure
 
Application has three files:
 - TaskList.elm - Elm implementation of the Task List web page (incl. Bootstrap styles)
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
hidden behind an additional library. I also did not need Bootstrap's JavaScript extensions, at least not yet.
This approach lets me have the latest Bootstrap version available at a hand. Having searched a bit more
I stumbled upon the following article:

https://bendyworks.com/blog/elm-frontend-right-now-updated-for-0-18

There we have a much more advanced Task List written by Brad Grzesiak and he also uses just plain <link> tags to
Bootstrap resources. 

### Third step - Final styling

The finishing touches included writing custom classes in style.css.


## Utilities
Here are some useful tools for Elm apps:
 - IntelliJ elm-plugin - http://durkiewicz.github.io/elm-plugin
 - elm-format - https://github.com/avh4/elm-format
   - IntelliJ support - https://github.com/durkiewicz/elm-plugin/issues/9

## Impressions

### First Impressions - Elm logic
Brilliant! With some background in functional programming it won't take much time to catch on with
Elm's syntax. Once you grasp the basics of its Html architecture (Model, View, Update) you are good to 
go with your first webpage. You specify the model and write a view function to represent it as
Html. With that in place you proceed with update functions that will keep your view 
and model in moving. Writing code that updates form field text in the application model 
was fairly simple to do right. Appending that text to an array of items was even simpler. 
What came to me as suprise, though, was that this was it - the page was ready, reacting
to changes, rendering correctly and working as expected. No testing, debugging had to be made -
I simply followed what compiler suggested. It was so much more convenient than fighting runtime
issues that are so common in most modern JS frameworks. Most of the things you normally fight at runtime 
Elm will not allow you to compile in the first place. If you attempt to hit a screw with a hammer Elm will
interrupt to instruct you to use a screwdriver instead. Your tools will stay intact, as 
will your application.

I used to code in OCaml but it did not give me the same confidence as Elm does. 
I know a bit of Haskell and Elm resembles Haskell a lot with its syntax, which I like
and I also find Elm much more modern and user-friendly than its 26-old ancestor. All in all,
I am looking forward to getting to know it better.
 
### Second Impression - Bootstrap

If you know Bootstrap then adding it to the Elm's Html hierarchy is very straightforward and the Elm Html tags
translate directly to corresponding plain Html tags. Not much more to add here, except that from what I have read
Bootstrap's JavaScript components are not in Elm yet. The thing is they are not so simple to integrate. 
Elm introduces its own apprach to interoperability with existing JavaScript libraries and there are still some 
bridges that need to be built. Truth be told, I have not found an Elm module that has a complete set of Bootstrap 
features covered, yet. If you find one - please let me know.

### Third Impression - Final styling

The last step was adding some finishing touches to the layouts. This meant writing some CSS
class definitions and surprisingly it was the toughest part for me. My CSS knowledge may have
become a bit rusty over last year but I did not expect to find it that tiring.
For me it was like driving off a freshly opened tarmac highway to a wet, muddy, unpaved dirt. 
Every little thing suddenly started to take way more time than it would expect it to take. 
Some heights not calculated, some aligns not working, some blocks not acting as blocks. 
Nothing was like in the crystal-clear world of functional Elm.  

This somewhat concludes my overall impression of the UI reality of past decade... The gap between Elm and CSS showed
me how different this new functional UI language is from the other, older UI technologies. My opinion
may be biased towards Elm because I do like functional languages and I do like Haskell (which Elm resembles) so 
I would really like to encourage you to try it out yourself and share your experiences.