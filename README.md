
# Noname - Telefone Lyric Ranker
This is a simple little application I made where users can submit and rank different lyrics from Noname's album Telefone.

![alt tag](https://github.com/lpercivalDEV/noname-telefone-lyric-ranker/blob/master/nonamePreview.png)

##Live Demo:
https://lyric-ranker-app.herokuapp.com/

## Installation
1. Clone my repo
2. Open your terminal and  run `npm install` to download the necessary node modules

## Usage
1. Once everything is downloaded, in the terminal run `npm run savage`
2. Open your browser and navigate to `localhost:3000` you should now be able to see and use my application! :)


## How It's Made:

**Tech used:** HTML, CSS, JavaScript, Node.js, MongoDB, Express, EJS

This application allows users to listen to the album "Telefone" by Noname, submit their favorite lyrics from said album, and then up or down vote other lyric entries.

I used EJS to make an HTML template file that could be easily populated later with entries from the Mongo database I created.

In the server.js file, there are several http requests that make the app function:


The "post" request tells the database what data to store in its list of objects based on my specifications. For example, I have it set up so that whenever a user submits their name and a lyric, there is a property in the object for `name` and a property for `msg` to hold those values. When the "get" request is sent, the object will contain the values for the name and message the user entered.

The "put" and "delete" requests make the `thumbUp`, `thumbDown`, and `delete` functionalities work. It sends a request to the server to update the values stored in those properties in the database whenever a user clicks on one of those icons. I also added a function to subtract the number of `thumbDown` values from the `thumbUp` values to end up with one final number. This is calculated before the response is printed to the DOM.

I also embedded a third-party media player from BandCamp so that users can listen to the artist's album on my app.

I created the gif file on the site from several PNG images using giphy.com to create a final gif file.
The "get" request communicates with the server to pull information from the database I created using MongoDB and mLab.

Credit: Leon Noel's 21 Savage repository: https://github.com/leonnoel/savage-demo


## Optimizations
If I had more time, one of the top features I would love to add is the ability to isolate what parts of the page refresh so that way users can listen to the album with no interruptions. The way the app is coded right now, any time a user interacts with one of the buttons (thumbUp/Down, submit, delete), a get request is inevitably sent to request the updated information from the database. This get request causes a page refresh which restarts the player to its default "paused" mode. This means that anytime a user is listening to a song and clicks to upvote/downvote/delete or submit a lyric, the page refreshes and the player stops playing music - super annoying.

Given more time, I would definitely switch the code around to use ajax requests instead of the http requests so that way the whole page does not refresh and the users can enjoy their tunes uninterrupted.

I would also like to improve the design of the app also. Right now it's not responsive, and I would love for it to work on mobile/tablet/smaller laptop screens.

## Lessons Learned:

This is the app that made me realize I can create full stack applications. After I got it to work - all sorts of ideas started popping up in my mind about what I could create next. I'm really grateful for the learning process I went through with this app because now I feel as if I can create anything.

## Examples:
Take a look at these couple examples that I have in my own portfolio:

coming soon...
