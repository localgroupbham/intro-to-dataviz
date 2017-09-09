# Introduction to Data Visualization 
Taught by Alan McConchie at Localgroup Studio

This document: https://github.com/localgroupbham/intro-to-dataviz


# Outline:


1 pm — **Part 1: Introduction to data visualization concepts and examples**

2 pm — **Part 2: Hands-on example: how D3.js works, how to build on code from bl.ocks.org and blockbuilder.org**

3 pm - 20 min break

4 pm - **Part 3: Working with CSS, handling data, enabling interaction and animation**

5 pm - Conclusion of class

# About this class: 

Obviously we could do a whole semester about data visualization. My goal in this class is to get you past the very first roadblocks so you can start to learn on your own.

This class will also be heavily directly by _your_ interests and questions. After the class I'll flesh out this document (https://github.com/localgroupbham/intro-to-dataviz) with more notes and links that we discussed today.

* What is data visualization?
* How it differs from data science
* How it differs from scientific visualization
* How is it different from infographics?

Fundamentally, dataviz is a combination of code and design. You can't really do it without using both.

There are so many kinds of visualizations! Some terminology:

* [Dataviz Catalogue](http://www.datavizcatalogue.com/)
* [Visualization types](http://guides.library.duke.edu/datavis/vis_types)
* [d3 gallery](https://github.com/d3/d3/wiki/Gallery)


Finally, today we're only talking about [D3.js](https://d3js.org/)

There are many other tools for dataviz. You can actually do a lot with excel, powerpoint, google sheets, etc. [Tableau](http://tableau.com) is the industry standard (but it's not free). [R](https://www.r-project.org/) is a popular open source statistics tool.

Why D3?

Unfortunately, it's got a steep learning curve. But it's become the de facto standard for data vizualization on the web. And because it's made up of HTML and CSS, and is completely customizable, it's great for designers (and artists) once they get the hang of it. So let's give it a try. 


# Part 2: Hands-on example

## Getting started

[Sign up](https://github.com/join) for a github account.

* Ok, what is [github](http://github.com)?
* What is [gist.github.com](http://gist.github.com)?
* What is [bl.ocks.org](http://bl.ocks.org)?
* What is [blockbuilder.org](http://blockbuilder.org)?
* Especially useful: [blockbuilder.org/search](http://blockbuilder.org/search)

## (At least) one thing you need to know about d3:
D3 recently transitioned from version 3 to 4. Check which version your examples are using, because some of the function names will be different. The syntax is basically the same. Look for `<script src="https://d3js.org/d3.v4.min.js"></script>
` or `<script src="https://d3js.org/d3.v3.min.js"></script>
` near the top of the example
      
  Some references about coding d3:
  
  * [_D3.js in Action_ book, by Elijah Meeks](https://www.manning.com/books/d3js-in-action-second-edition)
  * [Scott Murray's D3 Tutorials](http://alignedleft.com/tutorials/d3) (also a book)
  * [Ten Rules for Coding with D3](https://northlandia.wordpress.com/2014/10/23/ten-best-practices-for-coding-with-d3/)

## Build a bar chart

Anatomy of a d3 visualization: 

* HTML.
* Javascript.
* CSS.
* SVG (usually). 

All of this is part of the Document Object Model or "DOM". We'll look at each of these as we build our first visualization.

How data flows in d3:

* Notice d3 does [chaining functions](http://alignedleft.com/tutorials/d3/chaining-methods)
* How you ["bind data"](http://alignedleft.com/tutorials/d3/binding-data) to HTML features.
* How you [add, update, and remove](https://bl.ocks.org/mbostock/3808218) features.

Goals for this viz (I'll walk you through these)

1. Start with an empty [blockbuilder.org](http://blockbuilder.org) page
2. Download [this file of country data](https://gist.github.com/almccon/e47e8bab24d66e198b1737005664df26/raw/5e7e4fbcaf986482aea142414f84b5046808977e/gapminder_avg.csv) and add it to your block
3. Load the data into your visualization using d3.csv(), inspect it with console.log()
4. Display country names in your visualization
5. Display a bar chart of the country data

End result might be something like this:
[https://bl.ocks.org/almccon/e47e8bab24d66e198b1737005664df26](https://bl.ocks.org/almccon/e47e8bab24d66e198b1737005664df26)



# Part 3: CSS, handling data, enabling interaction and animation


This will depend on how far we got in Part 2, but we should be able to recreate this Hans Rosling style scatterplot:
    http://bl.ocks.org/dukevis/8782982

Try adding: 

* interaction (highight, then label, which is more complex)
* transitions (but you'll need to build a play button)

Need the full data?
Try this: https://github.com/romsson/dragit/blob/master/data/nations.json

Or get the raw data from here: http://www.gapminder.org/data/

## Advanced d3 (explore at home):

* [Simulations](https://bl.ocks.org/mbostock/4062045) (force directed layouts)
* [Canvas](http://blockbuilder.org/mbostock/2647922) (larger number of points possible)
* [SVG and CSS](http://bl.ocks.org/nbremer/0e98c72b043590769facc5e829ebf43f) effects (blobbly viz)


# Where to read more

People to follow in D3 and dataviz:

* [Mike Bostock](https://bost.ocks.org/mike/)
* [Nadieh Bremer](https://www.visualcinnamon.com/)
* [Elijah Meeks](http://elijahmeeks.com/)
* [Shirley Wu](http://sxywu.com/)
* [Irene Ros](http://www.ireneros.com/)
* [Ian Johnson](http://bl.ocks.org/enjalot)

Blogs and newsletters:

* [Information is Beautiful](http://www.informationisbeautiful.net/)
* [Dashing D3.js](https://www.dashingd3js.com/)
* [Flowing Data](http://flowingdata.com/)
* [Storytelling With Data](http://www.storytellingwithdata.com/)

New developments on the D3 horizon (it might be getting easier soon):

* [d3.express](https://medium.com/@mbostock/a-better-way-to-code-2b1d2876a3a0) under development by Mike Bostock
* [Semiotic](https://medium.com/@Elijah_Meeks/introducing-semiotic-for-data-visualization-88dc3c6b6926) just released by Elijah Meeks
