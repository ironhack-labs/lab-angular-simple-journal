![Ironhack Logo](https://i.imgur.com/1QgrNNw.png)

# Angular 2 & Express API | Simple Journal

## Introduction

![](https://s3-eu-west-1.amazonaws.com/ih-materials/uploads/upload_5bece35217249aa751825ce60429fb48.jpg)


Quite a few people keep a journal, as there are [many benefits to doing so](https://psychcentral.com/lib/the-health-benefits-of-journaling/), including better self awareness, stress relief, and increased problem solving capabilities.

Pen and paper can be great, but we're here to learn web development.

In doing so, we're going to create a personal journal using Angular 2, and an Express API.

## Requirements

- [Fork this repo](https://guides.github.com/activities/forking/)
- Clone this repo into your `~/code/labs`
- Include both the client and server applications in your submission.

## Submission

- Upon completion, run the following commands

```
git add .
git commit -m "done"
git push origin master
```

- Navigate to your repo and [create a Pull Request](https://help.github.com/articles/creating-a-pull-request/)

## Exercise

### Iteration 1 | API: Listing Entries

In the Express app included in the starter code, create a new model. This one and only model will be a `JournalEntry`.

This should include a `date`, `title`, and `content`.  **Make the date field's default today's date**.

Seed at least 10 fake journal entries in your database. Feel free to use [ipsum](http://www.lipsum.com/) text to fill in the content.

Finally, create an API route to retrieve all journal entries.

This route should be located at `/api/journal-entries`, and should response with a JSON array of objects of all journal entries in the database.

### Iteration 2 | Angular 2: Listing Entries

Create an Angular *service* to retrieve journal entries from your API.

Create an `entry-list` component which uses this service and find and display a list of your entries upon loading, with only the `title` and `date`.

Add the Angular router to your application. Create the home route which will make use of your `entry-list` component.

### Iteration 3 | API: Single Entry

Create a route mounted at `/api/journal-entries/:id` that will find and return a single entry from the database in JSON format.

### Iteration 4 | Angular 2: Single Entry

Add a method to your `journal-entries` service to retrieve a single journal entry from the API route that you've just created.

Create a `single-entry` component which finds a single entry from the API by it's ID, and displays the `title`, `date`, and `content`.

Finally, add a route to your Angular router, `/:id` which will render your single-entry component.

### Bonus | API: Creating Entries

Create an API route at `POST /api/journal-entries` that accepts a `title` and `content` as parameters, creates a new journal entry, and responds with the new object as JSON.

Make sure to include logic for sending an error back if the entry is not created.

### Bonus | Angular 2: Creating Entries

Add a new method to your service that takes in an object containing a `title` and `content`, and makes a POST request to the API route we've just created.

Create an `entry-form-component` and display it on the home page with the list of all of your journal entries. Optionally, add a button to show and hide the form.

Upon submission of this form, use your `journal-entries` service to make a POST request to the API and create the new entry.

Upon success of this submission, make sure the new journal entry is displayed on the home page.
