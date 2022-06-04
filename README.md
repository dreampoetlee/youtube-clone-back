# YouTube Clone Backend

## Learning Objective

Use Django REST Framework to build a REST API to serve as the backend for a YouTube Clone application with JWT user registration and login functionalities.

Repositories https://github.com/DevCodeCampInstructor/drf_jwt_backend

## Technologies

Django, Django REST Framework, MySQL, Postman

NOTE: Django REST API backend is for storing the comments for the videos. It is required to complete the backend API before moving on to any of the user stories. Once completed, send the GitHub repository with the completed code to private instructor chat to be checked off.

## User Stories
- As a developer, I want to make good, consistent commits (at least 25 for the entire team for both the backend and frontend).

- As a developer, I want to setup the Django + React starter code and connect the backend (Django API) to my MySQL database, closely following the setup guide for instructions.

- As a developer, I want to create a Comment model:

  - Property names must be in snake_case and match the following exactly!

    - user – ForeignKey

    - video_id – CharField

    - text – CharField

    - likes – IntegerField

    - dislikes – IntegerField

- As a developer, I want to create a Reply model:

  - Property names must be in snake_case and match the following exactly!

    - user – ForeignKey

    - comment – ForeignKey

    - text – CharField

- As a developer, I want to create a GET endpoint that does the following things:

  · Accepts a value from the request’s URL (The YouTube video id I am trying to get comments for).

  · Returns a 200 status code.

  · Responds with all comments from the database that are related to the video id sent in the URL.

- As a developer, I want to create a POST endpoint that does the following things:

  · Requires JWT authorization (Protected route).

  · Accepts a body object from the request in the form of a Comment model.

  · Adds the new comment to the database associated with the user who sent the JWT in the request.

  · Returns a 201 status code.

  · Responds with the newly created comment object.

- As a developer, I want to create a PUT endpoint that does the following things:

  · Requires JWT authorization (Protected route).

  · Accepts a value from the request’s URL (The id of the comment to be updated).

  · Accepts a body object from the request in the form of a Comment model.

  · Finds the comment in the Comments table and updates that comment with the properties that were sent in the request’s body.

  · Returns a 200 status code.

  · Responds with the newly updated comment object.

- As a developer, I want to create a GET endpoint that does the following things:

  · Requires JWT authorization (Protected route).

  · Accepts a value from the request’s URL (The id of the comment I am trying to get replies for).

  · Returns a 200 status code.

  · Responds with all replies from the database that are related to the comment id sent in the URL.

- As a developer, I want to create a POST endpoint that does the following things:

  · Requires JWT authorization (Protected route).

  · Accepts a value from the request’s URL (The id of the comment the reply will be connected to).

  · Accepts a body object from the request in the form of a Reply model.

  · Adds the new reply to the database associated with the comment id sent in the URL and the user who sent the JWT in the request.

  · Returns a 201 status code.

  · Responds with the newly created reply object.

- As a developer, I want to use Postman to make a POST, PUT, and both GET requests (get by id and get all) request to my REST web API, save it to a collection, and then export it as a JSON from Postman.