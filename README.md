# t3a2-a-pokeview
Full-Stack Web App part A - A place for Pokemon enthusiasts/trainers to review and rate their favorite Pokemon.

https://github.com/GeorgeNeocleous/t3a2-a-pokeview

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

## Target Audience
- The target audience of this web application will be for casual Pokemon fans, Pokemon enthusiasts and newcomers to Pokemon. It is designed to be simple, easy to explore and to find different pokemon.

![The website color pallete](./docs/Color%20Pallete.JPG)

- This color pallete was chosen due to its similarity to a Poke-Centre

## Dataflow Diagram

The navigation bar is present across all pages.
Comparison page, My List, Login, Home, Home (ordered by likes) etc.. can be navigated to by any page.

![Dataflow diagram with the relationship of each web-page](./docs/Dataflow%20Diagram.JPG)

- Yellow/orange boxes represent pages that require a user login for full functionality. Plain white boxes/grey represent single web pages accessible by regular visitors that have no significantly diminished functionality as a guest user. Home is green so that it stands out - relatively.

- Home is the page that will act as the default rendered webpage. This will contain buttons that allow the 151 Pokemon cards to be filtered by type, or, ordered by pokedex number and like number. 
- Comparison page will be where Pokemon stats and images can be observed side by side.
- Individual Pokemon page will allow access to likes, saving a Pokemon to their list and exclusive access to the sprite view page for that Pokemon. 
- My List page has the list of pokemon that has been saved by the user
- Login will allow users to login with their accounts but also give a potential user access to the register page (Login has a link to the registration page and the registration page has a link to the login page).
- The sprite view page is only accessible through the Individual Pokemon page.

![Dataflow diagram - login/register and the user database ](./docs/Dataflow%20Diagram%20(User%20verification).JPG)

- A new user will enter their proposed email, password and username. If these are valid values eg. valid email, password is not too short, username contains no profanity etc... then they are passed into the user database for secure storage.
- A user will then use the login page. This data will be passed to the database and checked for a match. If there is no match there were will be an error and a return to the login page re-prompting the user for their details.
- If there is a successful match then the database will return a JWT to the user.

## Application Architecture Diagram
![A diagram to show the app architecture](./docs/App%20architecture.JPG)

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

- User stories evolved over time and were refined to a degree. 

1st iteration
![User stories 1](./docs/User%20stories%201.JPG)

Final iteration
![User stories 2](./docs/User%20stories%202.JPG)
![User stories 2](./docs/User%20stories%202.1.JPG)

## Wireframes - Figma

![All wireframe pages - desktop views](./docs/Poke-view%20Figma%20hi-fid.JPG)

- This application is limited to desktop view for the moment but will be able to be expanded in the future.

![Wireframe - Homepage](./docs/Poke-view%20Default.JPG)

- The homepage contains cards, each representing an individual pokemon. By default, these are to be ordered by Pokedex number (1.Bulbasaur, 2.Ivysaur, 3.Venasaur, 4.Charmander...)
- In the navigation bar (barring the home link), there is "Compare", "Most Popular" and "My List". Additionally, there is a search bar which allows a user to find a Pokemon by Pokedex number, name or by type (yet to decide if it's necessary with the existence of the type filtering)

![Wireframe - Homepage (sorted by most likes)](./docs/Poke-view%20Home%20(Sorting%20by%20most%20liked).JPG)

- With a button, (yet to be added) users will be able to sort these cards by Pokedex number and like count (popularity). 

- The types menu on the right side will allow a user to select for types. If a user clicks on "Fire" only Pokemon that are fire-type will be shown on the page. It will be possible to reset this with a button (yet to be included).


![Wireframe - Single Pokemon page](./docs/Poke-view%20Pokemon%20single%20page.JPG)

- Clicking on a specific Pokemon on the Page will take the user to an individual Pokemon page.

![Wireframe - Sprite view for a single Pokemon](./docs/Poke-view%20Pokemon%20sprite%20view.JPG)

- When in the individual Pokemon page, a user will have a sprite view option. When clicked it will navigate the user to the sprite page for said pokemon and the page will be populated by almost all sprites available through Pokemon API (From 1st generation sprites to current)

![Wireframe - Comparison page](./docs/Poke-view%20Comparison.JPG)

- "Compare" will navigate the user to the comparison page. This will allow users to select different Pokemon to allow a side by side comparison (In statistics and design)

![Wireframe - My List page](./docs/Poke-view%20My%20List.JPG)

- "My List" is a page that will contain all the Pokemon that have been saved by the user. To allow for easy access and remembering their selection.
- Anywhere there is a Pokemon card, the user will see a thumbs up button, if that is clicked, then the pokemon card will now populate their "My List" page.

![Wireframe - Login page](./docs/Poke-view%20Login.JPG)
- Login is accessible by the "Login/Register" link on the right of the nav bar. A new user can navigate to the register page by clicking the register link or conversly the Login card will also have a prompt to "Create account", this will also link to the "Register" page.

![Wireframe - Create user/register page](./docs/Poke-view%20Register.JPG)

- The intention will also be that if a guest user attempts to complete an action that requires a login, then they will be prompted and redirected to login/register an account.



## Trello

- A green color represents an easy task, yellow is medium and orange is hard (in terms of effort - just more involved not necessarily "hard"). Green and yellow denotes something in-between the two. 
- Tasks were sorted by requirements and broken down into smaller tasks, such as user story 1, persona 1.

- The images below show how some of these tasks are split and how an iterative approach was utilised to complete this stage of the project using kanban.

![Trello - The initial setup for Trello before work has begun](./docs/Trello%20board%20(Kanban).JPG)

![Trello - Description of your website card (tasks)](./docs/R1%20-%20Description%20of%20your%20website.JPG)

![Trello - User stories card (tasks)](./docs/R4%20-%20User%20stories.JPG)



![Trello - Total view, most cards are in progress](./docs/Trello%20board%20(Kanban)%20(In-progress).JPG)

![Trello - User stories card (tasks 50% complete)](./docs/R4%20-%20User%20stories%20(DOING).JPG)

![Trello - Wireframes card (tasks 50% completed)](./docs/R5%20-%20Wireframes.JPG)



![![Trello - board view, all cards in progress or completed (1)]](./docs/Trello%20board%20(Kanban)%20(In-progress%202).JPG)

![Trello - board view, all cards in progress or completed (2)](./docs/Trello%20board%20(Kanban)%20(In-progress%203).JPG)

![Trello - board view, all cards in progress or completed (3)](./docs/Trello%20board%20(Kanban)%20(In-progress%204).JPG)

![Trello - board view, all cards completed](./docs/Trello%20board%20(Kanban)%20finished.JPG)


