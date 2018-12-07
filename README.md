# liri-node-app
Mimics liri in terminal using node

# Overview

LIRI is a Language Interpretation and Recognition Interface. LIRI is a command line Node.js app that takes in parameters and passes back data based on those parameters. LIRI searches Spotify for songs, Bandsintown for concerts, and OMDB for movies.

All data input by the user to the terminal is logged into log.txt using fs.appendFile in the logThis() function.

MUST use your own API keys.


# Installation required

[Node.js]
(https://nodejs.org/en/) 

[Node-File-System] 
(https://nodejs.org/api/fs.html)

[Axios]
(https://www.npmjs.com/package/axios)

[DotEnv] 
(https://www.npmjs.com/package/dotenv)

[JavaScript]
(https://www.javascript.com/)

[Moment.js]
(https://www.npmjs.com/package/moment)

[OMDB-API] 
(http://www.omdbapi.com)

[Bandsintown-API]
(http://www.artists.bandsintown.com/bandsintown-api)

[Node-Spotify-API]
(https://www.npmjs.com/package/node-spotify-api)



# How to use
![liri1](https://user-images.githubusercontent.com/43567870/49641287-8e3bf380-f9c4-11e8-8dd3-5f74dd6a10a4.png)




To search for upcoming concerts....



![liri3](https://user-images.githubusercontent.com/43567870/49641453-07d3e180-f9c5-11e8-8b70-87eb0ca25062.png)





node liri.js concert-this <artist/band-name>

This command searches the Bands in Town Artist Events API through Axios ("https://rest.bandsintown.com/artists/" + userQuery + "/events?app_id=" + keys.bands.id) and returns events the artist is appearing at in the near future. It includes Venue Name: , Venue Location: , and Date of the Event: . If no artist is entered, the API automatically searches Metallica for the user ;).

To search for song using Spotify....

node liri.js spotify-this-song <song-name>

This command searches the Spotify Web API that runs on Node.js (spotify.search({type: "track", query: userQuery}, function(err, data)) and returns information about the song the user input. It includes Artist: , Song Name: , and Preview Link: , and Album: . If no artist is entered, the API automatically searches "The Sign" by Ace of Base for the user.

TO search for a movie....
![liri2](https://user-images.githubusercontent.com/43567870/49641392-dce98d80-f9c4-11e8-81db-af042e2edfa0.png)




node liri.js movie-this <movie-name>

This command searches the OMDB API through Axios ("http://www.omdbapi.com/?t=" + userQuery + "&y=&plot=short&apikey=" + keys.movies.id) and returns information about the movie the user input. It includes Title: , Year Released: , IMDB Rating: , Rotten Tomatoes Rating: , Country/Countries Produced: , Language: , Plot: , and Cast: . If no movie is entered, the API automatically searches Mr. Nobody for the user, as well as letting them know that they should check it out, notifying the user that it's on Netflix, and providing a link to the IMDB page for the movie.

# Video example
Follow the link to view a brief demonstration of the app in action!
https://youtu.be/sn87JeXOv9w





