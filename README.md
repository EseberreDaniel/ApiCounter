# Android Development Challenge

## Before you begin
You will need to create a private GitLab repository using the information that we provided in this README and invite as collaborator: @JimenezR.

If you have any questions, please reach rodolfo.jimenez@umvel.com.

## The challenge
Create an Android app for counting things. You'll need to meet high expectations for quality and functionality. It must meet at least the following:

* Add a named counter to a list of counters.
* Increment any of the counters.
* Decrement any of the counters.
* Delete a counter.
* Show a sum of all the counter values.
* Search counters.
* Enable sharing counters.
* Handle batch deletion.
* Persist data back to the server.
* States are important, consider handling each state transition properly.
* Must **not** feel like a learning exercise. Think you're building it to publish for the Google Play Store, and you will change the world!.

Some other important notes:

* Showing off the knowledge of mobile architectures is essential.
* Offer support to Android API >= 21.
* Unreliable networks are a thing. Error handling is **expected**.
* The app should persist the counter list if the network is not available (i.e Airplane Mode).
* Create incremental commits instead of a single commit with the whole project **important**
* **Test your app to the latest Android API**

Bonus points:

* Don't bloat your Activities/Fragments.
* Minimal use of external dependencies.
* Tests are good: Unit, Instrumented, and UI. 
* Handle orientation changes.


**Remember**: The UI is super important. Don't build anything that doesn't feel right for Android.

***Use technologies and tools that make you feel good***


## Install, start and stop the server

#### Install server
```
$ npm install
```
#### Start server
```
$ npm start
```
#### Stop server
```
Ctr + c
```


## API endpoints / examples

> The following endpoints are expecting a `Content-Type: application/json`

```
GET /api/v1/counters
# []

POST {title: "shopping"} /api/v1/counter
# [
#   {id: "kyur6u4f", title: "shopping", count: 0}
# ]

POST {title: "water"} /api/v1/counter
# [
#   {id: "kyur6u4f", title: "shopping", count: 0},
#   {id: "sfur934f", title: "water", count: 0}
# ]

POST {id: "kyur6u4f"} /api/v1/counter/inc
# [
#   {id: "kyur6u4f", title: "shopping", count: 1},
#   {id: "sfur934f", title: "water", count: 0}
# ]

POST {id: "kyur6u4f"} /api/v1/counter/dec
# [
#   {id: "kyur6u4f", title: "shopping", count: 0},
#   {id: "sfur934f", title: "water", count: 0}
# ]

DELETE {id: "sfur934f"} /api/v1/counter
# [
#   {id: "C01", title: "shopping", count: 1}
# ]

GET /api/v1/counters
# [
#   {id: "C01", title: "shopping", count: 1}
# ]
```

> **NOTE:* Each request returns the current state of all counters.

# ApiCounter
