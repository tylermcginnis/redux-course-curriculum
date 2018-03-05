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

[Tyler](https://twitter.com/tylermcginnis)

## Step 2: First Actions
The first step you'll need to do in order to start building out your app is to fetch the initial data your app needs to render the home view. Before you can do that, you'll need to set up the actions and action creators responsible for doing that.

* Create an action creator responsible for setting the authenticated user (eventually set it to `tylermcginnis`, `sarah_edo`, or `dan_abramov`).
* Create an action creator you'll invoke after you receive the tweets from your API request.
* Create an action creator you'll invoke after you receive the users from your API request.
* Create an async action creator responsible for fetching the initial data of your app, then invoking your other action creators passing it that data.