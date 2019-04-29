# poke-ar-battlesim

This app will be a battle simulator for Pokemon in augmented reality

At the moment, it requires nothing to run, just access to camera. The method I've been using to test on my Android device was enabling developer options and USB debugging on my phone, finding my remote device on chrome devtools after connecting my device to my development machine via USB, using liveserver for VSCode and portforwarding for my remote device. 

Initial goal: create a pokemon damage calculator
Updated goal: create a pokemon battle simulator in AR

Examples: 
 - capstone that used unity, firebase, c# (not something i could do in 4 days), video of 2 people battling in AR
 - AR battle between 2 people
 - pokemon showdown
 
MVP: spawn 2 random or preset pokemon, give each 4 moves, allow user to select move on a UI, have a damage bar and show when a pokemon faints

Approach: pull necessary information off pokeAPI rather than creating a DB. alternatively, use a db already created, like from pokemon showdown

Struggles: One of the first AR libraries I found was AR.js. Although there is a lot of documentation and example projects with AR.js, I couldn't get it to do what I wanted. I lost 2 days with AR.js before learning about ARcore. I also had no idea on how to actually test what I was doing in AR. It took me a few hours to find a guide and hook my phone up to my computer to test AR. I was pretty stubborn on trying to get the AR to display gifs, as I preferred the aesthetic of in-game sprites to 3-D models. This proved to be a mistake as the documentation for the library needed to render gifs is nonexistent. After finally figuring out how to start using ARcore, I found some only pokemon models but in a less conventional format. Because of the way the model is set up, I was unable to convert the models textures, so currently the models are just these gray blobs. I then decided to try and render a menu to select moves, but it turns out that that's generally done in unity.

What I Learned: trying to learn new technologies is difficult, especially when I don't have a great foundation to begin with. I'm so used to having starting points and instructions that I get lost without them.

What I would do differently: After deciding on a goal, find as many example projects and guides as possible. If using a new technology, find and read about alternatives first. Spend less time researching irrelevant things.

Future features:
 - fully functioning battle sim
  - UI with move selection
 - preset pokemon and movesets
 - actual damage calculator
 - pokemon not locked relative to camera
 - pull from API rather than having a database
