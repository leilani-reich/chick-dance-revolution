# chick-dance-revolution

This project builds on skills in handling events and making javascript functions. Create a game where you are a dancing chick!

## Preliminary: Setting Up

- Download the img files 
- Create the files: index.html, styles.css, and app.js
- Upload the img folder into the directory you are working
- Set up and link the files

For the last step, follow these steps:
1. In your index.html file, initialize the file using the shortcut ```!```, then press tab. You should get something like the following.

``` html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <meta http-equiv="X-UA-Compatible" content="ie=edge">
  <title>Document</title>
</head>
<body>

</body>
</html>
```

2. Link your CSS and JS files as follows. You should have the link to the CSS stylesheet within the head tags
and the JS script within the body tags to ensure your CSS and JS are linked properly.

``` html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <meta http-equiv="X-UA-Compatible" content="ie=edge">
  <link rel="stylesheet" href="styles.css">
  <title>Document</title>
</head>
<body>

  <script src="app.js"></script>
</body>
</html>
```

## Part 1: HTML

1. Create the following HTML elements, following the nested structure.

- div with the id "container". This div will hold all our elements.
  - h1 with the inner HTML "Dance Chick Revolution".
  - div with the id "game". This div will hold all game elements.
    - div with the id "gameBoard". This div will hold chick and the dancefloor.
    - div with the id "musicBoard". This div will hold the music note arrows.
      - div with the id "topNotes". This div will hold the arrows at the top of the music board.
      - div with the id "moveNotes". This div will hold the arrows at the bottom of the music board, which will move up to the top.
  - button with the id "play" and inner HTML "Play". This button will start the game.
  - div with the id "score". This div will hold the score text.
    - h2 with the id "score-text" and the inner HTML "Score: 0". This div represents the score text.

Your HTML should look like this:

```
  <div id='container'>
    <h1>Dance Chick Revolution</h1>
    <div id='game'>
      <div id='danceBoard'></div>
      <div id='musicBoard'>
        <div id='topNotes'></div>
        <div id='moveNotes'></div>
      </div>
    </div>
    <button id='play'>Play</button>
    <div id='score'>
      <h2 id='score-text'>Score: 0</h2>
    </div>
  </div>
```

2. Add the following within each of the respective divs:

div with id "danceBoard":
```
   <img src="blue-arrow.png" alt="blue arrow" id='arrow-upperleft' class='arrow'>
        <img src="blue-arrow.png" alt="blue arrow" id='arrow-up' class='arrow'>
        <img src="blue-arrow.png" alt="blue arrow" id='arrow-upperright' class='arrow'>
        <img src="blue-arrow.png" alt="blue arrow" id='arrow-left' class='arrow'>
        <img src="img/chick-base.png" alt="chick" id='chick'>
        <img src="blue-arrow.png" alt="blue arrow" id='arrow-right' class='arrow'>
        <img src="blue-arrow.png" alt="blue arrow" id='arrow-lowerleft' class='arrow'>
        <img src="blue-arrow.png" alt="blue arrow" id='arrow-down' class='arrow'>
        <img src="blue-arrow.png" alt="blue arrow" id='arrow-lowerright' class='arrow'>
```

The above code adds arrow elements to the dance board where the chick will be dancing.

div with id "topNotes":
```
<img src="blue-arrow.png" alt="blue arrow" id='toparrow-up' class='toparrow'>
          <img src="blue-arrow.png" alt="blue arrow" id='toparrow-right' class='toparrow'>
          <img src="blue-arrow.png" alt="blue arrow" id='toparrow-down' class='toparrow'>
          <img src="blue-arrow.png" alt="blue arrow" id='toparrow-left' class='toparrow'>
```

The above code adds arrow elements to the music board. These are the arrows at the top of the board that don't move.

div with id "moveNotes":
```
          <img src="blue-arrow.png" alt="blue arrow" id='movearrow-up' class='movearrow'>
          <img src="blue-arrow.png" alt="blue arrow" id='movearrow-right' class='movearrow'>
          <img src="blue-arrow.png" alt="blue arrow" id='movearrow-down' class='movearrow'>
          <img src="blue-arrow.png" alt="blue arrow" id='movearrow-left' class='movearrow'>
```

The above code adds arrow elements to the music board. These are the arrows at the bottom of the board that will move upwards.

## Part 2: CSS

Next up, head to your style.css file. We are going to add style to our elements.

1. Main elements styling

Copy the below code and follow the directions in the comments.

```
body {
  /* Set the background image to farm.jpg */
}

#container {
  /* Set the position to fixed. This will ensure no elements move out of place. */
}

#chick {
  /* Set height and width to 250px */
}

h1 {
  /* Style title font how you want */
}

#game {
  /* Set the display to flex. This will help organize the main divs */
}

#danceBoard {
  /* Set border to 2px solid black */
  /* Set height and width to 750px */
  /* Set background color to reasonable color like gray */
  /* Set the left margin to 300px. This helps position the dance board correctly. */
}

#musicBoard {
  /* Set border to 2px solid black */
  /* Set height to 750px and width to 700px */
  /* Set background color to reasonable color like orange */
  /* Set right margin to 300px */
  /* Set display to flex */
  /* Set justify content to center */
}
```

2. Arrow elements styling

Copy the below code and follow the directions in the comments.

```
.arrow {
  /* Set height and width to 240px */
}

#arrow-up {
 /* Set transform to rotate(180deg) */
}

#arrow-upperright {
  /* Set transform to rotate(225deg) */
  /* Set opacity to 50% */
}

#arrow-right {
  /* Set transform to rotate(-90deg) */
}

#arrow-lowerright {
  /* Set transform to rotate(-45deg) */
  /* Set opacity to 50% */
}

#arrow-lower {
  /* Set transform to rotate(90deg) */
}

#arrow-upperleft {
  /* Set transform to rotate(135deg) */
  /* Set opacity to 50% */
}

#arrow-left {
  /* Set transform to rotate(90deg) */
}

#arrow-lowerleft {
  /* Set transform to rotate(45deg) */
  /* Set opacity to 50% */
}

.toparrow, .movearrow {
  /* Set height and width to 150px */
}

#toparrow-up, #movearrow-up {
  /* Set transform to rotate(90deg) */
  transform: rotate(90deg);
}

#toparrow-right, #movearrow-right {
  /* Set transform to rotate(-90deg) */
}

#toparrow-down, #movearrow-down {
  /* Set transform to rotate(0deg) */
}

#toparrow-left, #movearrow-left {
  /* Set transform to rotate(90deg) */
}

#topNotes {
  /* Set display to flex */
  /* Set self align to flex-start */
}

#moveNotes {
  /* Set opacity to 80% */
}

#movearrow-up {
  /* Set position to absolute */
  /* Set bottom to 500px */
  /* Set right to 800px */
}

#movearrow-right {
  /* Set position to absolute */
  /* Set bottom to 500px */
  /* Set right to 650px */
}

#movearrow-down {
  /* Set position to absolute */
  /* Set bottom to 500px */
  /* Set right to 500px */
}

#movearrow-left {
  /* Set position to absolute */
  /* Set bottom to 500px */
  /* Set right to 350px */
}
```

This code sets up some important formatting for the arrows. For example, we transform our arrows to point them in the correct direction.
The movearrows are going to be animated and will need keyframes. This brings us to the next step.

Copy the below code and follow the directions in the comments. If you are stuck, follow the formatting [here](https://www.w3schools.com/cssref/css3_pr_animation-keyframes.php).

```
@keyframes moveUp {
  /* Have the keyframe go from bottom: 500px to bottom: 1100px */
}

@keyframes moveLeft {
  /* Have the keyframe go from bottom: 500px to bottom: 1100px */
}

@keyframes moveDown {
  /* Have the keyframe go from bottom: 500px to bottom: 1100px */
}

@keyframes moveRight {
  /* Have the keyframe go from bottom: 500px to bottom: 1100px */
}
```

3. End elements styling

Finally, we must add styling to our play button and score text so that they appear on the page correctly and neatly.
Copy the below code and follow the directions in the comments.

Style the play button
```
#play {
  /* Set left and bottom margins to 300px */
  /* Set the display to inline block */
  /* Style the font size, background color, border radius, color, etc.
}
```

Style the score text
```
#score {
  /* Set left margin to 900px */
  /* Set bottom margin to 300px */
  /* Set the display to inline block */
  /* Set height to 200px */
  /* Set width to 300px */
  /* Style the font size, background color, border radius, color, etc.
}
```

## Part 3: JS

Now we are finally into the JavaScript section. Head to your script.js file and follow along.

1. Set up variables
- Create variable for chick 
- Create variables for elements with ids arrow-up, arrow-left, arrow-right, arrow-down
- Create variables for elements with ids movearrow-up, movearrow-left, movearrow-right, movearrow-down
- Create variable for score text
- Create empty array variable called "moves" for holding game moves



