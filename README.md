# VueJS Todo Application - CSoC Dev Web Task 3

## Introduction

In this task you will be working on a todo application made using NuxtJS a SSR framework for VueJS. The main motive of this task is to make you familiar with:

- Life Cycle Hooks in VueJS
- Data Fetching and Rendering
- Component Creation
- Custom Events
- Class Binding
- State Manegment

## Setting up the project

Follow the following steps to setup this project.

**Note** : 
- This task requires [pnpm](https://pnpm.io/) which is a new tooling similar to npm that you encountered in last task.
- In case of any dependency errors while installing using npm, use this command instead
  ```
  npm install pnpm --legacy-peer-deps
  ```

### Setup this repository

First of all, click on the top-right corner of this repository to fork it. Then you can clone your fork on your system locally.

### Run the server

Install the dependencies using

```
pnpm i
```

Then you can finally run the server using this command.

```
pnpm run dev
```

Then you can go to `localhost:3000` in your browser.

### Deploying App

You can use netlify or vercel for deploying your app. The build command is

```
pnpm run build
pnpm run generate
```

This will create a `dist` folder which can be served now

## Todo Application

There are three pages in this site.

- `/` - This is the main page where the user can create, edit or delete the tasks.
- `/login` - This is the login page.
- `/register` - This is the register page.

We have also created a backend server containing the API endpoints required for this application to function completely - [https://todo-api-s7vj.onrender.com/](https://todo-api-s7vj.onrender.com/)

You can find [the documentation](./API_Documentation.md) of the endpoints in this repository itself.

## Tasks

You would notice that the application is not functional completely. So, your task is to make it completely functional. You would be working in :

- [Landing](./pages/index.vue)
- [Register](./pages/register/index.vue)
- [Login](./pages/login/index.vue)
- [Add Task](./components/addTask.vue)
- [Auth Middleware](./middleware/auth.ts)

There are several todos mentioned in these files. You have to complete those.

In particular you have to

- **Auth middleware** - You may notice that initially you are landed on the main page even when you are not logged in. That is wrong. In [auth.ts](./middleware/auth.ts) you have to add the logic for redirection based on he/she/them is authenticated or not. You will also be require to integrate your middleware into pages/router.

- **Login Function** - Currently only register function works. You have to complete the login function too present in [Login](./pages/login/index.vue). And then change the state in store.

- **Get Tasks function** - There is a function `getTasks` in [Index](./pages/index.vue). You would notice that even after logging in, you see two tasks _Sample Task 1_ and _Sample Task 2_. These tasks were not created by you. These are dummy tasks. You have complete the `getTasks` function such that the tasks listed are the ones created by the user.

- **Add Task** - This functionality is spread over two functions [addTask](./component/addTask.vue) and [fetchTask](./pages/index.vue) which you have to complete by making API call and finally adding element to DOM.

- **Delete Task function** - This functions is present in the [Index](./pages/index.vue) file. You have to complete it.

- **Update Task** - This functions is present in the [Index](./pages/index.vue) file. To complete this you have to add in functionality for class binding/ conditional rendering to toggle elements. Finally complete the `updateTask` function.

- **UI Improvement** - Add in trasition for list by using vue transition component and combining css transitions.

## Points

Here is the breakdown of the points related to each task.

| **Task**        | **Points** |
| --------------- | ---------- |
| Auth Middleware | 10         |
| Login Function  | 15         |
| Add task        | 25         |
| Get tasks       | 30         |
| Update Task     | 40         |
| Delete Task     | 20         |
| UI Improvement  | 10         |
| **Total**       | 150        |

## Judging

Judging would be done on the basis of your implementation and authenticity.

## Deadline

You'll have a week to complete this task. Hence, the deadline of this task is **9th July, 2023**.

## Submission

- Follow the instructions to setup this project.
- Complete the task by making the required changes in the files.
- When done, commit your work locally and push it to your origin (forked repository).
- Make a pull request to our repository, stating the tasks which you have completed.
- Let us review your pull request.
