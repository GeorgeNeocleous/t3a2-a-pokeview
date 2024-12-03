# t3a2-a-pokeview
Full-Stack Web App part A - A place for Pokemon enthusiasts/trainers to review and rate their favorite Pokemon.

## Purpose
- The purpose of this web application is to provide users/visitors with a cool space to appreciate 1st generation Pokemon. Visitors will also be able to observe the popularity of Pokemon - voted by the user base or create a list of Pokemon for whatever reason they please whether it is favourite Pokemon, Pokemon they've caught in game, or Pokemon they just like the look of.
- Make a list of Pokemon which could reflect the Pokemon they have caught or Pokemon they want to find or just have a general interest in. 
See almost all available sprites accessed through the Pokemon API, to see how the design has changed as new games have come out.

## Functionality/Features
- Search function (by name or number)
- Filtering by pokemon type
- Ordering the list by popularity (like count)
- Create a list of pokemon
- Look at pokemon stats
- Compare multiple pokemon
- Look at how a specific pokemons sprites have been designed over different games
- Create a user account to allow authorisation to features such as building a list and liking pokemon

![Poke-view Figma hi-fid](./Color%20Pallete.JPG)

- This color pallete was chosen due to its similarity to a Poke-Centre

## Dataflow Diagram

### Site map
The navigation bar is present across all pages.
Comparison page, My List, Login, Home, Home (ordered by likes) etc.. can be navigated to by any page.

![Poke-view Figma hi-fid](./Dataflow%20Diagram.JPG)

- Yellow/orange boxes represent pages that require a user login for full functionality. Plain white boxes/grey represent single web pages accessible by regular visitors that have no significantly diminished functionality as a guest user. Home is green so that it stands out - relatively.

- Home is the page that will act as the default rendered webpage. This will contain buttons that allow the 151 Pokemon cards to be filtered by type, or, ordered by pokedex number and like number. 
- Comparison page will be where Pokemon stats and images can be observed side by side.
- Individual Pokemon page will allow access to likes, saving a Pokemon to their list and exclusive access to the sprite view page for that Pokemon. 
- My List page has the list of pokemon that has been saved by the user
- Login will allow users to login with their accounts but also give a potential user access to the register page (Login has a link to the registration page and the registration page has a link to the login page).
- The sprite view page is only accessible through the Individual Pokemon page.

![Poke-view Figma hi-fid](./Dataflow%20Diagram%20(User%20verification).JPG)

- A new user will enter their proposed email, password and username. If these are valid values eg. valid email, password is not too short, username contains no profanity etc... then they are passed into the user database for secure storage.
- A user will then use the login page. This data will be passed to the database and checked for a match. If there is no match there were will be an error and a return to the login page re-prompting the user for their details.
- If there is a successful match then the database will return a JWT to the user.

## Application Architecture Diagram


## User Stories

### Persona 1: Steve (Serious gamer)
- Occupation: Accountant
- Age: 32
- Goals: To build the strongest Pokemon team to dominate all the trainers in the game but also to dominate real players in PvP. Wants to see what all the fuss is about.
- Background: Plays Call of Duty in amateur competitions. Can't stand losing.

### User story 1: 
- As a serious pokemon gamer, I want to be able to search for different pokemon by name or by type, see their stats and compare them against each other, so I can find Pokemon that I think will be the strongest for my strategy.

### Persona 2: Joel (Casual Pokemon Enthusiast/Card Collector) 
- Age: 15
- Occupation: High School student
- Goals: Wants to start playing with the first generation of Pokemon, but first he wants to find his favourite Pokemon and see what everyone else likes.
- Background: Became interested in Pokemon by collecting cards, now he wants to try the early games so he wants to do some research.

### User story 2: 
- As a Pokemon enthusiast, I want to create a list of Pokemon and their evolutions so that I can find a team of Pokemon that I like.

### Persona 3: Rebecca 
- Occupation: Game developer/designer
- Age: 29
- Goals: To find inspiration in game design, specifically in sprite design.
- Background: A game developer who grew up with pokemon and wants to see if they can find inspiration in one of their favourite games. Loves the older pixel art style of Pokemon.
  
### User story 3: 
- As a game developer/designer, I would like to see the different graphical designs/sprites of Pokemon and how they've changed as new games have come out, so that I can gain insight on what made them so great and memorable.

## Wireframes - Figma

![Poke-view Figma hi-fid](./Poke-view%20Figma%20hi-fid.JPG)

- This application is limited to desktop view for the moment but will be able to be expanded in the future.

![Poke-view Figma hi-fid](./Poke-view%20Default.JPG)

- The homepage contains cards, each representing an individual pokemon. By default, these are to be ordered by Pokedex number (1.Bulbasaur, 2.Ivysaur, 3.Venasaur, 4.Charmander...)

![Poke-view Figma hi-fid](./Poke-view%20Home%20(Sorting%20by%20most%20liked).JPG)

- With a button, (yet to be added) users will be able to sort these cards by Pokedex number and like count (popularity). 

- The types menu on the right side will allow a user to select for types. If a user clicks on "Fire" only Pokemon that are fire-type will be shown on the page. It will be possible to reset this with a button (yet to be included).


![Poke-view Figma hi-fid](./Poke-view%20Pokemon%20single%20page.JPG)

- Clicking on a specific Pokemon on the Page will take the user to an individual Pokemon page.

- In the navigation bar (barring the home link), there is "Compare", "Most Popular" and "My List". 

- Compare will navigate the user to the comparison page. This will allow users to select different Pokemon to allow a side by side comparison (In statistics and design)

![Poke-view Figma hi-fid](./Poke-view%20Comparison.JPG)

- 




![Poke-view Figma hi-fid](./Poke-view%20Pokemon%20sprite%20view.JPG)



![Poke-view Figma hi-fid](./Poke-view%20My%20List.JPG)

![Poke-view Figma hi-fid](./Poke-view%20Login.JPG)

![Poke-view Figma hi-fid](./Poke-view%20Register.JPG)

## Trello

![Poke-view Figma hi-fid](./Trello%20board%20(Kanban).JPG)

![Poke-view Figma hi-fid](./R1%20-%20Description%20of%20your%20website.JPG)

![Poke-view Figma hi-fid](./R4%20-%20User%20stories.JPG)

![Poke-view Figma hi-fid](./R5%20-%20Wireframes.JPG)



![Poke-view Figma hi-fid](./Trello%20board%20(Kanban)%20(In-progress).JPG)

![Poke-view Figma hi-fid](./R4%20-%20User%20stories%20(DOING).JPG)

![Poke-view Figma hi-fid](./R5%20-%20Wireframes%20(DOING).JPG)




![Poke-view Figma hi-fid](./Trello%20board%20(Kanban)%20(In-progress%202).JPG)

![Poke-view Figma hi-fid](./Trello%20board%20(Kanban)%20(In-progress%203).JPG)

![Poke-view Figma hi-fid](./Trello%20board%20(Kanban)%20(In-progress%204).JPG)

![Poke-view Figma hi-fid](./Trello%20board%20(Kanban)%20finished.JPG)


