# StoryHunter

### Group 37; Hanna Almqvist, My Andersson, Frida Jansson & Hanna Snarberg

#### DH2642

[Click here to reach deployed application!](https://storyhunter-2a3c7.web.app/)

## Description of the project

StoryHunter is the website that will help you find your new favourite series! On the website the user can see a list of popular series, search for series, add series to their watch list, get recommendations based on a title and if the user is feeling adventurous, they can get a randomized suggestion. The idea of StoryHunter is to make it easy for users to browse series to find their next one!

## Setup

Make sure that you are inside the `Project-Group-37/storyhunter` folder when performing the following!

### Add config files

```
Project-Group-37/storyhunter/scr/apiConfig.js
Project-Group-37/storyhunter/scr/firebase.config.js
```

### Install dependencies

```
npm install
```

### Run project

```
npm start
```

### Build project

```
npm run build
```

## Project file structure

#### Project-Group-37

-   .prettierrc: Specifications on how we want to format our code

#### Project-Group-37/storyhunter

**- build: a production build of our website, which optimizes for best performance**
**- node_modules: contains libraries downloaded from the npm install**

-   .firebaserc: file that stores our project alias.
-   .gitignore: states which files will be ignored by git.
-   firebase.json: file define which files in our project directory that should be deployed to our firebase project
-   package-lock.json: keeps track of the dependency trees
-   package.json: lists the packages the app depends on
-   README.md: describes our project and also some “getting started with Create React App”-info that we got when downloading create react app.

#### Project-Group-37/storyhunter/.firebase

-   hosting.YnVpbGQ.cache: this file is to recognize the last changes in the deploy, this is to minimize the time and size of deployment.

#### Project-Group-37/storyhunter/public

-   favicon.ico: a picture of our logo,
-   index.html: default page shown of our website
-   logo192.png: a picture of our logo
-   logo512.png: a picture of our logo
-   manifest.json: also included, a file that tells the browser about your website on the user's mobile device or desktop.
-   robots.txt: also included, a file that tells search engine crawlers which URLs the crawler can access on your site.

#### Project-Group-37/storyhunter/src

-   .gitIgnore: states which files will be ignored by git.
-   App.js: here we create our model and here we handle when to show the different views.
-   App.test.js: file for testing the app. It was included in the create react app setup.
-   SeriesModel.js: the model that handles primarily the adding and removing from the users watchlist, but it is also here that currentSeries is stored and updated when the user clicks on the image of a series on the website. Also the observers are added, removed, stored and notified using the model
-   authContext.js: use context handling authentication
-   firebasemodel.js: contains our firebasemodels, for example how we fetch data from firebase
-   index.js: Here the app is rendered
-   reportWebVitals.js: Included in the create react set up. A tool for measuring the real life performance of the app
    .
-   seriesSource.js here is where the API calls happen. Different functions to fetch certain data from different endpoints are included.
-   setupTests.js: imports jest-DOM

#### Project-Group-37/storyhunter/src/CSS

the CSS files for each view. They set the layout of the different views.

-   App.css
-   afterRandom.css
-   afterSimilar.css
-   authentication.css
-   beforeRandom.css
-   beforeSimilar.css
-   button.css
-   crossIcon.css
-   details.css
-   header.css
-   index.css
-   load.css
-   overview.css
-   searchIcon.css
-   searchResults.css
-   show.css
-   starIcon.css
-   watchList.css

#### Project-Group-37/storyhunter/src/Custom-hooks

-   useModelProp.js: Allows us to track states of the model properties
-   usePromise.js: Handles promises using state, returns the data or error that a promise gives.

#### Project-Group-37/storyhunter/src/Icons

-   crossIcon.js: imports 'x' icon from FontAwsomeIcon
-   searchIcon.js: imports search icon from FontAwsomeIcon
-   starIcon.js: imports star icon from FontAwsomeIcon

#### Project-Group-37/storyhunter/src/Presenters

-   showPresenter.js: Handles whether to hide a view or not depending on the state of window.location.hash
-   detailsPresenter.js: returns detailsView, sends props to the view depending on the state of the SeriesModel
-   headerPresenter.js: returns headerView
-   logOutPresenter.js: returns logOutView
-   loginPresenter.js: returns loginView
-   overviewPresenter.js: returns overviewView
-   randomizePresenter.js: returns beforeRandomizeView or afterRandomizeView depending on if a randomization has occured or not
-   registerPresenter.js: returns registerView
-   searchResultPresenter.js: returns searchResultView
-   similarSeriesPresenter.js: returns beforeSimilarView or afterSimilarView depending on if a similar search has occured or not
-   watchlistPresenter.js: returns the watchlistView

#### Project-Group-37/storyhunter/src/Views

-   afterRandomizeView.js: the view after randomization of a series has occurred, shows a randomized series after button press by the user
-   afterSimilarView.js: the view after a similar-series-search has occured, shows a similar series to what the user decided to search by (if more than one similar-series is found, the user can press a button to go through the results)
-   beforeRandomizeView.js: the view before randomization of a series has occured, shows a randomize button
-   beforeSimilarView.js: the view before a similar-search has occured, shows a search bar and a button
-   detailsView.js: the view of how detailed information about a series is presented, displays information after clicking on a series image
-   headerView.js: the header at the top of the page, containing a search bar where the user can search for series and a logout-button
-   loginView.js: the view the users sees when logging in
-   logoutView.js: the view that pops up when the user wants to log out
-   overviewView.js: shows trendy or high rated series which the user can toggle between by pressing a button
-   promiseNoData.js: handles promises, and returns a loading gif while it is still pending
-   registerView.js: the view where the user can register a new account
-   searchResultsView.js: shows series based on what the user searched for (in the search bar placed header)
-   watchListView.js: In this view the watchlist that placed to the left side on the website is built up with image, title, a star icon, and functions to add and remove from the watchlist.
