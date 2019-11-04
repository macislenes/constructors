# constructors

 ## What is WordGuess and a quick overview:

WordGuess is like a modern day hangman you can play in the console. We itterate through an array of movie titles and display blank spaces in place of the letters for you to guess what letter goes where.  

This game will help you get familiar with how to log things in the console as well as retreive and manipulate input data
 
## WordGuess can perform the following actions:
```"Game"```
A function that initiates our gameplay in the console it contains several game functions within to run the game, including:
* play
* askForLetter
* MakeGuess
* askToPlayAgain
* nextWord

```"play"```
An action that sets our guesses to 10 and retreives the next word

```”askForLetter”``` 
An action that lets you see tour dates and locations for a band such as:
* Venue Name
* Venue Location
* Date of Concert

```"makeGuess"```
An action that returns information from OMDb on a movie of your choice, including:
* Movie Title
* Release year
* IMDb Rating
* Rotten Tomatoes Rating
* Country
* Language
* Plot

```"askToPlayAgain"```
An action that returns song information from spotify for a search term of your choice, including:
* Artist(s)
* Song name
* Song preview URL
* Album


```"nextWord"```
This action will run the action specified in the file random.txt and return the information for any of the actions above.



 
## Looking at the code:
* **liri.js:** All the main functionality of the app. The entry point for the application.
* **.gitignore:** File which instructs git to ignore the files contained in it
* **key.js:**  A module that loads the spotify API keys from the environment and is used by liri.js
* **package.json**: NPM information and dependencies

 
## Unpacking liri.js:
The application is divided into three sections
* First Section: Requiring our modules and identifying the "operation" and "searchTerm"
    * "operation" ==> the action specified in the command line (spotify-this, etc.)
    * "searchTerm" ==> what we are searching for ("Backstreet Boys", "Forrest gump", etc.)

* Second Section: There are two functions for each operation, one to call the API and one to parse the response and display it
    * ```getMovieDetails()```
    * ```parseMovieResponse()```
    * ```getBandDetails()```
    * ```parseBandResponse()```
    * ```getSongDetails()```
    * ```parseSpotifyResponse()```

* Third Section: This section identifies what action is required to be taken based on the command line input, and calls the respective function.
 
## Start to Finish:
Here's how you can use LIRIbot!

1. Search for Tour Dates:
    ```node liri.js concert-this "Snoop Dogg"```
    What to expect:
![concert-this](images/spotify.png)
2. Search for song details:
    ```node liri.js spotify-this-song "I want it that way"```
    What to expect:
![spotify-this-song](images/snoopdogg.png)
3. Search for movie details:
    ```node liri.js movie-this "Princess Bride" ```
    What to expect: 
![movie-this](images/princessbride.png)
4. File input:
    ```node liri.js do-what-it-says```
    What to expect: 
![do-what-it-says](images/backstreetboys.png)


Designed and developed by: Maci Slenes
