# React-Launchpad
    My project is a single page launchpad using ruby rails and React. The board is displayed on the landing page, and each click of each individual tile generates a sound, and lights up when the state of the tile has been changed. I will refer to each tile as an item now, because of my programming naming convention. The program renders a list through React, and the list is composed of 25 items, which are also rendered in React.In the list there is an array of objects with the properties of Tile and Audio. Tile refers to the name of the Item, and Audio is the name of the file that is accessed through the asset pipeline to render the sound. The asset pipeline manages the audio files loaded in the sound folder.Through the Rails.root, we are able to access the root directory path of our files. This makes it easier to call upon and mange the sound files for each of our items. We then setup out items component, assigning Item with a key and item. Our rendered list with all the items can now be displayed in our Application.js.jsx.
    We have mapped out the list, and now we will get into the details of the items in that list. Each item starts out with an initial state of clicked as false, and has the properties of tile and audio, as well as a key. When the item is in a false state the background of each item is white. There is a function in the items called handleClick, which takes a key argument, and modifies the state of that specific item based on the key passed to it. When called upon the clicked state of that specific key will be changed to true. The audio portion is handled by the playSound function, which finds the ref sound and plays the audio from the src inside the audio tags. When the div is clicked, the playSound function is called upon through onClick. This triggers the audio. The tile then lights up if the state of the item is true, when clicked is true change will be appended to the class name, and in the css file there is a color_me.change class, which render the background a different color. The item now changed color onMouseDown, and returns when onMouseUp, this is because the handle click is switch on and off.

    Contributions to be made could be something as simple as sound engineering practices or techniques. Also better mp3 files that users can share and append to the program. On a more technical level, maybe completing the stretch challenge, which was having an Amazon S3 bucket hold the files that users upload so that they can customize their own launchpad.

    To get the program to work, clone the repo, run bundle install, then setup the rails server and you are good to go.(git clone, bundle install, rails s).
