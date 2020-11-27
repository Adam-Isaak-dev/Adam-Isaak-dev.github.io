---
layout: post
title:  "Coding a simple puzzle game"
date:   2020-11-22 20:44:00 -0600
categories: blog-post writing-task
image: /assets/images/writing-task-6-pic.png
---

Through this post, I’m going to cover a simple puzzle game that I finished for an assignment in javascript.

The puzzle game itself is a simple card matching game. You are given a set of twelve random cards and then need to find the one that matches the given card. This process repeats until all the cards have been matched. The fewer guesses it takes you the better your score.

Simple enough right? Let’s dive in and figure out what’s going on behind the screen.

## The three core parts
This program revolves around three key parts:
* A function resets the game board upon loading the page or pressing the reset button.
* A function checks if the user has matched the card upon clicking.
* A function checks to see if the user has won.

### Resetting
The reset functionality follows the following process:  
![reset flowchart](/assets/20-11-22/flowchart_1.png)

*Reset Flowchart*

### Click functionality
When the user clicks anywhere in the browser window we do the following:
``` javascript
if (event.target.tagName != "LI" || event.target.classList.contains('matched') || event.target.classList.contains('show')) {
    return;
}
```
What this code does is that if the user hasn’t clicked on a card, or a card that is already shown or matched, it ends the current function. If that doesn't happen then we hide the old shown card, and then set the card we clicked on to shown. As written here:
``` javascript
for (let i = 0; i < cards.length; i++) {
  if(cards[i].classList.contains('show')) {
    cards[i].classList.remove('show');
  }
}

event.target.classList.add('show');
``` 
We then add to the score, then check to see if the selected card matches the card we are supposed to find. To do this we simply compare the current card and the target of our click, then if they match, set the target to be matched rather than shown.

Next comes a complicated part of the program. We need to keep track of the cards the user has to search for so that we don’t have to look for one they have already matched. It boils down to randomly selecting a card, and then checking to see if it matches any of the ones we have already used, if it does try again, if not then set the selected card to next.

### Win validation
In addition to the previous functionality, whenever the user clicks on a card we have the program check to see if the user has won by matching all the cards. To do this first we check every single card and see if it is ‘matched’. If they are matched we add that to a count. That code looks like this:
``` javascript
let matchedCount = 0;
for (let i = 0; i < cards.length; i++) {
  if(cards[i].classList.contains('matched')) {
    matchedCount++;
  }
}
```
Once we have the total number of matched cards, we check to see if that number matches the number of cards we have. If they match alert the user, if not do nothing. That looks like this:
``` javascript
if (matchedCount == cards.length){
  setTimeout(function(){alert(`You won with a score of: ${document.getElementById('score').innerText}`);}, 0);
}
```

## Conclusion
The following diagram is an overview of the whole functionality of the game:
![program flowchart](/assets/20-11-22/flowchart_2.png)

*Program Flowchart*

To summarize the functionality once more, the three primary components of the program are a reset function to reset the game, a click function that reacts if the user clicks on cards and either matches it or sets it to show, and finally a function that checks to see if the user has won.


> *Splash Image by [Boskampi](https://pixabay.com/users/boskampi-3788146/?utm_source=link-attribution&amp;utm_medium=referral&amp;utm_campaign=image&amp;utm_content=1873854) from [Pixabay](https://pixabay.com/?utm_source=link-attribution&amp;utm_medium=referral&amp;utm_campaign=image&amp;utm_content=1873854)*