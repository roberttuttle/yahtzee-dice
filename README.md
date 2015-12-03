# Yahtzee Dice

The result of rapid DIY macgyvering while in mid-flight with kids needing entertainment which turned into an educational piece on the power of modern web UI technologies and basic coding patterns

## Demo
https://rawgit.com/frog/yahtzee-dice/master/html5-yahtzee-dice.htm

## Story

While traveling for the Thanksgiving holiday (November, 2015), my two young girls (8 and 6) were blissfully seated
in a row of three together with their Mommy for one segment of our flight from Texas to California on Southwest Airlines. 
A promise was made that on the next segment they would sit with Daddy and be ready for an entertaining game of Yahtzee 
(a game that I introduced them to recently to inject some additional math practice outside of their homework from school)
having already exhausted the other activity options of interest on the current flight. A quick check of supplies revealed 
that the game score sheets and a pencil were packed, but no dice (pun intended) on the actual dice to play. 
Heartbreak ensued with about an hour and half left before the first stop.

But since I can code for the modern web, it was HTML5, CSS3, SVG, and JavaScript to the rescue!

The Wi-Fi on board was out, so pulling down my usual toolbox of optimized frameworks like jQuery, LESS, and others was not an option. 
I was at 39,000-feet armed only with syntax memory, some basic intellisense within Visual Studio Code (my current editor of choice), 
and a web browser to run a local file. It was going to be an adventure in raw CSS and vanilla JavaScript to get the job done and save the day. 
Adding insult to injury as I attempted to draw some SVGs for the die faces, Adobe CC Illustrator barfed up an error saying my license has expired 
or is corrupt and I needed to connect to my Adobe cloud account to fix it. It bailed and I also had to code SVGs by hand directly in XML.

Fortunately, my Microsoft Surface Pro 3 passed the "tablets can stay open" rule with the flight staff and allowed me to keep coding right as we 
pulled up to the gate for the quick turnaround to our next flight. As we settled in for our next flight, I was armed with virtual 3D Yahtzee dice 
on a touch screen and the kids are ready to play. Exhibiting typical behavior that comes from being the children of a frog, it turned out they were 
more interested to tell me how it should work for them (real-time user feedback and validation!) and understanding how these dice were just like the 
real thing and the game would be the same. I was able to get them to grok the basic concepts of random number generation and three-dimensional space 
in the context of building and rolling physical dice and we were off and running. Games were played and code was tweaked in between. 

The single file of code and markup (293 lines) in this repo and the UI it offers is the result of this in-flight near-drama turned into a personal hackathon for me and an educational experience for my kids. 

More about the game of Yahtzee for the uninitiated: https://en.wikipedia.org/wiki/Yahtzee

Have fun!

## Instructions

* Open the HTML file in a local browser offline or from the online demo link provided above (works in most modern desktop and mobile browsers ... I used Microsoft Edge on my Surface Pro 3 touchscreen with the kids)
* Roll the dice
* Tap or click on any dice you want to keep
* Roll again (and/or again) (optional, of course)
* Score your Yahtzee turn per game rules (paper sheets available separately ... search for them on the interwebs)
* Reset the dice to move on to the next turn

## What's Going On In The Code & Markup?

* Lines 288 - 290: our random number generator in JavaScript (we need a 1 through 6 for our standard dice)
* Lines 203 - 207: JavaScript array to hold the state info on our virtual dice (we need 5 dice and 3 rolls for per turn in Yahtzee)
* Lines 150 - 185: hand-coded SVG vector symbols for the 6 faces for our virtual dice
* Lines 189 - 198: the HTML markup containing the template for one die and its 6 faces
* Lines 86 - 120: CSS transforms to render the 6 faces of our die into proper 3D space to construct our cube
* Lines 62 - 85: CSS transforms to orient the 3D cube with the proper face showing based on the current value of the die
* Lines 211 - 229: initialization to create and render our 5 virtual dice on to the screen based on the template
* Lines 231 - 259: "roll" the dice! Spend one second randomly spinning the dice around and then land on random values generated.
* Lines 271 - 276: toggle die selection when one is tapped or clicked by the player
* Lines 278 - 286: keep track of the rolls remaining in a player's turn and disable the control when turn is over
* Lines 261 - 269: reset the dice and start the next player's turn
