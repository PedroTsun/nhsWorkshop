# Adding Styling to Webpages

After composing a html file with your important content ready to be published on the world wide web,
you may want to make your webpage look good. This would mean adding styling to make
your webpage look presentable. In the following example, you will get to
know more about styling and in particular you will see why we want to have CSS (cascading style sheet)
on webpages.

## Preparing to add styling

* open a web browser and go to [replit](https://replit.com/)
* Log in (with your google account)
* Create a new replit project by clicking on the blue button near the top left of the page
* Search and select html/css/js
* In your html file, go to between the body tags: ` <body> </body> `
* Make your own list in the body or copy the following list into the body.
```html
<ul>
    <li> Alex's Adventures In Numberland </li>
    <li> Gulliver's Travel</li>
    <li> Animal Farm</li>
    <li> What's the Point of Math?</li>
    <li> The Jungle </li>
    <li> Beyond Infinity </li>
    <li> The Calculus Story </li>
    <li> 1984 </li>
    <li> Mathematics and the Imagination </li>
    <li> Fahrenheit 451 </li>
    <li> The Canterbury Tales </li>
</ul>
```
* We will spend most of our time on this list or your own list. It may not seem like much, but less is really more in this case.


## In-line Styling
* Say you want to highlight the two types of books in your list. You can use styling to set different color.
* You may want DarkOrange for math books and mediumSeaGreen for fiction books.
* For example, `<li style="color: DarkOrange;"> Alex's Adventures In Numberland </li>`
* For a fiction, `<li style="color: mediumSeaGreen;"> Gulliver's Travel</li>`
* Use the above two examples, set the book titles to the corresponding color.

## CSS (Cascading Style Sheet)
* One day you want to change the colors to DodgerBlue and Tomato.
* You could do it by hand. However, if you have a tendency to change color frequently, there is a better way.
* Copy the below list and add it after the first list.
```html
<ul>
    <li class = "mathBk"> Alex's Adventures In Numberland </li>
    <li class = "englishBk"> Gulliver's Travel</li>
    <li class = "englishBk"> Animal Farm</li>
    <li class = "mathBk"> What's the Point of Math?</li>
    <li class = "englishBk"> The Jungle </li>
    <li class = "mathBk"> Beyond Infinity </li>
    <li class = "mathBk"> The Calculus Story </li>
    <li class = "englishBk"> 1984 </li>
    <li class = "mathBk"> Mathematics and the Imagination </li>
    <li class = "englishBk"> Fahrenheit 451 </li>
    <li class = "englishBk"> The Canterbury Tales </li>
</ul>
```
* However, you will find that the new list has no color. You need one more thing.
* Between the `<head> </head>`, add the following to specify a value for the CSS property of a class:
```html
  <style>
    .mathBk {
      color: DodgerBlue
    }
    .englishBk {
      color: Tomato
    }
  </style>
```
* Voila, you have done CSS. Nice Work! CSS allows you to specify a change in one place, and the change will propagate to every element that is designated with that class name.

## Some Useful Things to have on Your Webpage
* Have a list of links
* Have an image link in addition to a text link
* Have a class that sets text font or text size to selected items on your webpages


## Useful Resources
* [w3schools](https://www.w3schools.com/)
* [khan academy web design](https://www.khanacademy.org/computing/computer-programming/html-css)
* [Learning web design : a beginner's guide to HTML, CSS, Javascript, and web graphics](https://www.barnesandnoble.com/w/learning-web-design-jennifer-niederst-robbins/1112357082?ean=9781491960202)
[]: # '[A Guide to Markdown File](https://towardsdatascience.com/the-ultimate-markdown-cheat-sheet-3d3976b31a0)'