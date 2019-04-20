# [French Montana - No Stylist (feat. Drake)](https://www.youtube.com/watch?v=9_k_goMr5ZI)

## ** Disclaimer: This project has NOOOOOO styling. This was a showcase of my knowledge in building a RESTFul API and building a fullstack application. The only styling is what was required for the exam.

Here are the to the [basic requirements](https://github.com/joinpursuit/PCNW-Web-Final)

###### Please note there are no instructions on how to create the Genres link shown in the mockups nor are their instructions on how to display the Post page.

### /frontend: React

The project has a few **pages** which are as follows:

#### Home

Route: ```/```

The home page only serves to display a welcome message.

![alt text](https://github.com/nadavgreen/unit-6-final/blob/master/assests/home.png "home")

#### Users 

Route: ```/users```

The users page lists all of the users in the db. If the button **next** to the users name is pressed, the correcponding user is now the **active user**. Pressing a user directly will take you to their page regardless of if they are the active user.

![alt text](https://github.com/nadavgreen/unit-6-final/blob/master/assests/users.png "users")

#### User

Route: ```/user/:id```

The user/:id page list all of the shows watched by the selected user *(not only the active user)*. You can select the image of the show to go to the shows page.

![alt text](https://github.com/nadavgreen/unit-6-final/blob/master/assests/userShows.png "userShows")

#### Post

Route: ```/user/post```

The user/post page allows an **active user** to upload a show they have watched. This form takes a **title**, a **image url** and a selected **genre** from a pre-created list

![alt text](https://github.com/nadavgreen/unit-6-final/blob/master/assests/post.png "post")

#### Show

Route: ```/show/:id```

The show/:id page list the currently selected show. Showcasing the image, tile and genre.

![alt text](https://github.com/nadavgreen/unit-6-final/blob/master/assests/show.png "Show")

#### 

Route: ```/shows```

The /shows page list all of the tv shows in the database and the users that are watching them directly **below**

![alt text](https://github.com/nadavgreen/unit-6-final/blob/master/assests/tvShows.png "tvShows")

In this example, after a **post**, [Pam Beesley](https://www.youtube.com/watch?v=gO8N3L_aERg) has created the [Lion King](https://www.youtube.com/watch?v=4CbLXeGSDxg) show as can be seen **below**.

![alt text](https://github.com/nadavgreen/unit-6-final/blob/master/assests/editedTvShows.png "editedTvShows")

### /backend: Express

##### The practice server was not implemented with CI/CD, unit testing, nor validation

###### Endpoints return '{"msg":"passed"}', '{"msg":"failed"}' or '{"msg":data}' where applicable

**Endpoints:**

**Route: ```/users```**

Post: ```/create```

The create endpoint on the users path allows you to post a new user. The only required data is a username

```data = { username: "YOUR DATA" }```

```curl -X POST http://localhost:3001/users/create -H "Content-Type: application/json" -d '{"username":"YOUR DATA"}'```

GET: ```/read/:id```

The read/:id endpoint on the users path allows you to get a specific user based on id

```id = YOUR DATA```

```curl http://localhost:3001/users/read/:YOUR DATA```

GET: ```/read```

The read endpoint on the users path allows you to get all users in the db. No data is required

```data : null```

```curl http://localhost:3001/users/read```

PUT: ```/update```

The update endpoint on the users path allows you to put new information of an existing user. The only required data is a username

```data = { username: "YOUR DATA" }```

```curl -X PUT http://localhost:3001/users/update -H "Content-Type: application/json" -d '{"username":"YOUR DATA"}'```

DELETE: ```/delete```

The delete endpoint on the users path allows you to delete the information of a specific user based on id

```data = { id : YOUR DATA }```

```curl -X DELETE http://localhost:3001/users/delete``` -H "Content-Type: application/json" -d '{"id":"YOU DATA"}'

**Route: ```/genres```**

**Route: ```/shows```**


The update endpoint on the users path allows you to put new information of an existing user. Because this is a **put** you will have to enter **all** information even if you aren't making changes to that column

**Route: ```/comments```**
