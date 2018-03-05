<img src="https://tylermcginnis.com/tylermcginnis_glasses-300.png" width="300" align="right">

Redux Twitter (Curriculum)
========

#### This is the curriculum for TylerMcGinnis.com's [Redux course](https://tylermcginnis.com/courses/redux/)

## Objective
Build a functioning Twitter like application. You can play around with the [final app here](https://tylermcginnis.com/projects/redux-twitter/).

## Notes
The goal here is to give you just enough guidance for you to struggle without drowning. Note that the steps below are just suggestions. The ideal situation is you look at the completed project, then you build it. However, if you're not up for such things, feel free to follow the (vague by design) steps below. If you get stuck, all steps have coinciding branches for you to reference as a last case scenario.

## Step 0: Examine the Final Product
 * Head over [HERE](https://tylermcginnis.com/projects/redux-twitter/) and play around with the final project. Think about how you'd structure not only your UI, but also your Redux store.

## Step 1: Download the starter code
Just like we did in the Polls app, we're going to "mock" the database/server.

* Clone this repositoty
* Check out the given code
* Get comfortable with the exports in `api.js` and `helpers.js`.
* You'll use the `formatTweet` method as a format step between the structure of a tweet in the "database" and the structure of a Tweet in your Redux store.

## Step 2: First Actions
The first step you'll need to do in order to start building out your app is to fetch the initial data your app needs to render the home view. Before you can do that, you'll need to set up the actions and action creators responsible for doing that.

* Create an action creator responsible for setting the authenticated user (eventually set it to `tylermcginnis`, `sarah_edo`, or `dan_abramov`).
* Create an action creator you'll invoke after you receive the tweets from your API request.
* Create an action creator you'll invoke after you receive the users from your API request.
* Create an async action creator responsible for fetching the initial data of your app, then invoking your other action creators passing it that data.

## Step 3: First Reducers

* Create the reducers which are going to update the store based on the action creators you created in the last step.
* Create a store and use react-redux's Provider component to put it on context.

## Step 4: Middleware
In order for your async action creators (thunks) to work, you'll need to enable them as middleware.

* Build a logger middleware.
* Enable your logger middleware and the redux-thunk middleware in your store.

## Step 5: Initial Data
Now that you have your action creators, reducers, and middleware set up, now you need to actually fetch your initial data.

* Invoke your action creator which handles fetching the initial data.

At this point, you should have no UI but you should have an authed user, the users, and the tweets in your store.

## Step 6: Dashboard
Now is time to start working on the UI

* Create a new component that receives all the Tweet Ids from the store and renders them.
* Render your new component in the main App.js file only once the data has been loaded.

<img src='https://user-images.githubusercontent.com/2933430/36964134-ec8ee9e2-2012-11e8-9077-129200194da2.png' width="400" />

## Step 7: Tweet UI
Now instead of just rendering IDs, you want to render the full Tweet UI.

* Build a Tweet component that takes in an ID, grabs that tweet (using the ID) from the store, and renders whatever UI you'd like.

<img src='https://user-images.githubusercontent.com/2933430/36964638-84dff24e-2014-11e8-86c0-d916e55a2842.png' width='400px' />

## Step 8: Loading
You don't just want to show a blank UI as your app loads.

* Download the `react-redux-loading` library.
* Hook up the loading state to your reducer and show a loading indicator as your app is loading.

## Step 9: Like Tweet
Now that the UI is set up for liking a Tweet, you need to build out that functionality.

* Build out the proper action creators you'll dispatch when a user likes a tweet.
* Update your tweets reducer to handle the new actions you just created.
* Dispatch your new action creator when a Tweet is liked.

## Step 10: Compose Tweet UI
Now we want to be able to add a new Tweet.

* Create the UI for a component which allows the user to input a new Tweet.
* Render that component.

<img src='https://user-images.githubusercontent.com/2933430/36965834-134fcf1a-2018-11e8-9928-91e5f45b0f0b.png' width='400' />

## Step 11: Compose Tweet Logic
Now that you have the UI for creating a new Tweet, the next step is adding in the logic.

* Create your actions for handling adding a new Tweet. Remember the `saveTweet` method from your API.
* Update your tweets reducer to handle the new actions you just built.
* Dispatch your new action creator when a new Tweet is created.

## Step 12 : Tweet Page
Now the only last view in our app we need is the individual Tweet page.

* Create a new component which renders the proper UI in the image below. Remember you'll need to render any replies to that Tweet as well.

Eventually you'll use React Router to render this route, for now, render it like this and you'll be able to grab `match.params.id` for the Tweet id just as React Router will give you.

```js
<TweetPage match={{params: {id: '8xf0y6ziyjabvozdd253nd'}}}/>
```

<img src='https://user-images.githubusercontent.com/2933430/36966017-9da4aed8-2018-11e8-936f-e3c82461647d.png' width='400' />

## Step 13: React Router
Now, the last step is to dynamically render UI based on the URL. You can use React Router to do this.

* install `react-router-dom`
* Create a navbar you can render to navigate between views.
* Add in `Route`s so you only render certain components on certain paths.
* Redirect to `/` after the user composes a new Tweet.
* Navigate to the individual Tweet page when a user clicks on a Tweet.

[Tyler](https://twitter.com/tylermcginnis)
