Using pandoc to produce [reveal.js](http://lab.hakim.se/reveal-js/) slides

You can use pandoc to produce slides using reveal.js.

First, create a reveal.js template: Edit the demo file index.html in the [reveal.js repository](http://github.com/hakimel/reveal.js). Remove everything inside the <div id="slides">, and replace it with $body$. Save this as template.revealjs.

Now use this command to produce your slide show:

pandoc --section-divs -t html5 -s --template template.revealjs -o myslides.html myslides.txt
You'll need the js, lib, and css directories from the reveal.js repository in the same directory as myslides.html.

See also [this gist](https://gist.github.com/aaronwolen/5017084).

NOTE: The development version of pandoc (and the next release) contain direct support for revealjs, including its 2D features.