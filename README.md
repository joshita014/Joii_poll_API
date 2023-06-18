# Joii_poll_API

Joii_poll_API is a Polling API which is an Open Application. 
<br>
Joii_poll_API is created by using Express, Nodejs, MongoDB.


## Features

- Users can create questions (you can add as many questions as you want).
- Users can add options to a question.
- Users can add a vote to an option of question.
- Users can delete a question -> A question can't be deleted if one of it's options has votes.
- Users can delete an option -> An option can't be deleted if it has even one vote given to it.
- Users can view a question with it's options and all the votes given to it.


## To run the project on your local machine:

1. Open terminal.

2. Change the current working directory to the location where you want the cloned directory.

   ```
   $ git clone https://github.com/kartiksarwan2017/Polling_System_API

   ```

3. Install all the dependencies by running :

   ```
   npm install

   ```

4. Run npm start to run the project at local host, port 8000:

   ```
   $ npm start

   ```


## We are using Postman to test these API's

The following is the link to be used in Postman:-

### API to Create a question: 
        http://localhost:8000/questions/create

### API to Add options to a question: 
        http://localhost:8000/questions/:id/options/create

### API to Add a vote to an option of question: 
        http://localhost:8000/options/:id/add_vote

### API to Delete an Option: 
        http://localhost:8000/options/:id/delete

### API to Delete a question: 
        http://localhost:8000/questions/:id/delete

### API to View a question with it’s options and all the votes given to it: 
        http://localhost:8000/questions/:id
        


Example:-
```json
{
  "id": 1,
  "title": "Who is your favorite from the Ninjas Mentors",
  "options": [
    {
      "id": 1,
      "text": "Ankush Singla",
      "votes": 100,
      "link_to_vote": "https://localhost:8000/options/:id/add_vote"
    }
  ]
}
