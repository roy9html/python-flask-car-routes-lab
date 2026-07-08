# Lab: Car Routes Lab

---

## Overview

Now it is time for you to build your own routes!

You are building routes for a car company database. You will need to build:

- A **default route** introducing the company
- A **model-specific route** for requesting information on a car model

---

## Tasks

### Task 1: Define the Problem

Build routes for a car company:

- `/` (default route)
- `/<model>` (route for a specific car model)

---

### Task 2: Determine the Design

#### App Routes:

- `GET /`
- `GET /<model>`

---

### Task 3: Develop the Code

- Initialize Flask
- Set up `/` route
- Set up `/<model>` route

---

### Task 4: Test and Refine

- Debug and test during development using the provided test suite and Flask instance

---

### Task 5: Document and Maintain

- Commit as you go, writing meaningful commit messages
- Push commit history to GitHub periodically and when the lab is complete

---

## Tools and Resources

- **GitHub Repo**: [https://github.com/learn-co-curriculum/python-flask-car-routes-lab](https://github.com/learn-co-curriculum/python-flask-car-routes-lab)
- **Flask Quickstart**: [https://flask.palletsprojects.com/en/stable/quickstart/](https://flask.palletsprojects.com/en/stable/quickstart/)

---

## Instructions

### Set Up

Before we begin coding, complete the initial setup:

1. **Fork and Clone**
   - Go to the GitHub repository link.
   - Fork the repository to your GitHub account.
   - Clone the forked repository to your local machine.

2. **Open and Run**
   - Open the project in VSCode.
   - Run `pipenv install` to install dependencies.
   - Run `pipenv shell` to open a Python shell instance.

---

## Task 1: Define the Problem

Build the following routes:

- Default Route: `/`
- Model Route: `/<model>`

---

## Task 2: Determine the Design

### App Routes:

- `/`  
  - Returns: `"Welcome to Flatiron Cars"`

- `/<model>`  
  - Takes `model` variable from the URL  
  - Uses the `model` variable to check against an `existing_models` array  
    - If model exists:  
      `"Flatiron {model} is in our fleet!"`  
    - If model doesn't exist:  
      `"No models called {model} exists in our catalog"`

---

## Task 3: Develop, Test, and Refine the Code

1. Create a **feature branch**
2. Build the following:

### `/` Route

- Returns: `"Welcome to Flatiron Cars"`

### `/<model>` Route

- Accepts a model name from the URL
- Uses the model variable to check the `existing_models` array
  - If found: return `"Flatiron {model} is in our fleet!"`
  - If not found: return `"No models called {model} exists in our catalog"`

3. Push the feature branch and open a PR on GitHub
4. Merge into `main`

---

## Implementation Notes

The Flask app in `server/app.py` exposes two routes:

- `/` returns a welcome message: `Welcome to Flatiron Cars`
- `/<model>` checks the requested model name against the `existing_models` list
  - If the model exists, the app returns `Flatiron {model} is in our fleet!`
  - If the model does not exist, the app returns `No models called {model} exists in our catalog`

## Demo Screenshot

Below is a screenshot of the application structure and an example response for `GET /Crossroads`.

![Flatiron Cars Routes](screenshot.png)

---

## Task 4: Document and Maintain

### Best Practices:

- Add comments explaining logic and purpose
- Clarify code intent for future developers
- Include a screenshot of completed work in the README
- Update README to reflect functionality using [https://makeareadme.com](https://makeareadme.com)
- Delete stale GitHub branches
- Remove unused or commented-out code
- Update `.gitignore` to exclude sensitive data (if needed)

---

## Submission

Once all tests are passing and code is pushed to the `main` branch:

- Submit your GitHub repo through **Canvas** using **CodeGrade**

---

## Grading Criteria

- Application passes all test suites
- `/` route is created and returns correctly
- `/<model>` route is created and returns correctly
