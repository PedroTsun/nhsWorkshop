# Making Your Webpage Interactive

In this tutorial, the author assumes that you know html and css. If you are
unfamiliar with html and css, you should do the lessons/workshops on html and css.
Once you have made a webpage, you probably want your webpage to do something more
useful than just displaying information. To learn how to make your webpages
do work for you, you will need to learn javascript. For people unfamiliar with
javascript, it looks like an impossible challenge to learn javascript, but you
will be engaged in a journey of making your mulitple choice questions interacting
with your customers (learners). The audience for this workshop could be anybody;
a teacher will find it useful, a student studying for a subject may find the lesson
helpful to learning, even a parent or tutor may find this lesson useful for preparing
students to do well on exams.



## Preparing to write your javascript program

* open a web browser and go to [replit](https://replit.com/)
* Log in (with your google account)
* Create a new replit project by clicking on the blue button near the top left of the page
* Search and select html/css/js
* In your html file, go to between the body tags: ` <body> </body> `
* Type the html content below in the body or copy the following marked-up text into the body.
```html
  <div style="padding-left: 1em; position: relative;">
    <span id='y2023janQ1fb'>&nbsp;&nbsp;&nbsp;</span>
    <select id="y2023janQ1">
      <option value="0"></option>
      <option value="1">1</option>
      <option value="2">2</option>
      <option value="3">3</option>
      <option value="4">4</option>

    </select>
    1. Which conclusion was developed as a result of
the gold foil experiment?<br>
    <ul style="list-style-type: none">
      <li>(1) Atoms are mostly empty space.</li>
      <li>(2) All atoms are hard, indivisible spheres.</li>
      <li>(3) Atoms have different volumes.</li>
      <li>(4) All atoms have the same volume.</li>
    </ul>
    <br>
  </div>
```



* We just finished putting the question on a webpage. Now, we turn our attention to adding interactivity to the webpage.


## Javascript: DOM events
* The javascript (JS) code below may look like gibberish, but there are just three steps to it.
* First, select the html element that you want to use. In this case, choose the html option select tag.
* Second, specify the event that will trigger a reaction: A change in the select option is chosen as an event.
* Third, spell out what to do once the event has occurred. In this case, once a different option is selected, a function called choiceSelected() will be invoked to check if the answer is correct and to give feedback on the html page. 
```html

  <script>
    var y2023janAnsKeys = {};
    y2023janAnsKeys.y2023janQ1 = [];
    y2023janAnsKeys.y2023janQ1[0] = "y2023janQ1";
    y2023janAnsKeys.y2023janQ1[1] = 1; // The correct answer is choice 1

    function choiceSelected(evt) {
      let userSelectedChoice = parseInt(evt.target.value);
      let elVisibleFB = document.querySelector(evt.currentTarget.FB);
      if (userSelectedChoice === evt.currentTarget.answer) {
        elVisibleFB.innerHTML = "&#10004;";
        elVisibleFB.style.color = "limeGreen";
      } else if (userSelectedChoice === 0) {
        elVisibleFB.innerHTML = "&nbsp;&nbsp;&nbsp;";
      } else if (userSelectedChoice != evt.currentTarget.answer) {
        elVisibleFB.innerHTML = "&#10006;";
        elVisibleFB.style.color = "red";
      }
    }

    var elQ1 = document.querySelector("#" + y2023janAnsKeys.y2023janQ1[0]);
    elQ1.answer = y2023janAnsKeys.y2023janQ1[1];
    elQ1.FB = "#" + y2023janAnsKeys.y2023janQ1[0] + "fb";
    elQ1.addEventListener("change", choiceSelected);
  </script>


```

* This quick tutorial is not meant to teach you javascript in details. It gives you an
example of how JS can be useful. To learn more, you can learn by watching some useful khan academy videos on JS. 

## Some Suggestions for JS on Your Webpage
* Have a multiple choice that gives hints
* Have the webpage tally the number of correctly answered multiple choices. 
* Have a flashcard on webpages


## Useful Resources
* [khan academy JS](https://www.khanacademy.org/computing/computer-programming/html-css-js)
* [An example of MC in JS](https://www.freecodecamp.org/news/multiple-choice-quiz-template/)
* [Javascript Workout](https://www.freecodecamp.org/learn/javascript-algorithms-and-data-structures/#basic-javascript)
<!--- [A Guide to Markdown File](https://towardsdatascience.com/the-ultimate-markdown-cheat-sheet-3d3976b31a0) --->