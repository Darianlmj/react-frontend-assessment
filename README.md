# CSESoc Projects React Frontend Assessment

### Magic White Powder Inc.

In this assessment, you will be asked to build the frontend for a online shopping website that sells different kinds of white powder 👀. 

**Note: Although this assessment is optional, we highly encourage applicants to complete it or at least make a decent attempt in completing it. Who knows, you might learn something new and interesting from it.**

<p align="center">
  <a href="#getting-started">Getting Started</a> •
  <a href="#specifications">Specifications</a> •
  <a href="#extension">Extension</a> •
  <a href="#assumptions">Assumptions</a> •
  <a href="#submission">Submission</a>
</p>

***

<h2 id="getting-started">1. Getting Started 😎</h2>

If you do not have `pnpm` installed, you can do so by running the command `npm install -g pnpm`. Then verify it by running `pnpm --version`.

Starting up the frontend
1. Fork this repository into your own GitHub account.
2. Navigate to the `/frontend` directory and run `pnpm install`.
3. Run `pnpm run start`.
4. Open a browser and go to the URL provided.

Starting up the backend
1. In a seperate terminal, navigate to the `/backend` directory and run `pnpm install`.
2. Run `pnpm run start`.

***

<h2 id="specifications">2. Specifications 🔧</h2>
Completion of this part of the assessment is required.

### 2.1 Displaying Products
In this section, you will need to display the different products that the store sells.

#### 2.1.1 Getting the available products
A route has been provided for you in `backend/` that will return a list of all the products that are available. You will need to display the products with all of their associated information (i.e. the product's image, name, description and price).

#### 2.1.2 Removing a product from view
A button should also be placed at the bottom of each product that when clicked, removes the product from the page. Think of it as "hiding" a product. Upon removing the product, the remaining products should realign themselves to fill the space left by the removed product.

### 2.2 User Authorisation
As of now, we are assuming that any user is able to remove products from view. However, in reality, we would want to ensure that only an admin of the website can remove it.

You will notice that there is a login button in the navigation bar of the page. When clicked, this button is supposed to authenticate a predefined user and allow them to remove products from view.

#### 2.2.1 Getting a token
A route has been provided for you in `backend/`. This route will authenticate the user and return a token that can be used to remove products from view.

You will need to implement the login functionality such that when the Login button is pressed, the admin will get logged in. In addition, you will need to refactor your code to the point where only the admin can remove products from view. If the admin is not logged in, the "remove" button should not be visible.

#### 2.2.2 Logging out
When the admin logs in, the Login button should switch to a Logout button. Upon logout, the Remove button should also disappear. 

#### 2.2.3 Pass the Token
Something about using useContext to handle the token.

### 2.3 Janky Component
There exists a component called `NavigationBar` which contains far too many chunks of code that are become a bit of an eyesore. You task is to refactor the code in this component file. How you do this is up to you.

***

<h2 id="extension">3. Extension 🏗️</h2>
Completion of this part of the assessment is optional. However, bonus points for completion!!!

### 3.1 TypeScript > JavaScript
You might be wondering, why the heck is the frontend even in JavaScript while the backend gets more love and attention with TypeScript being used for it? Well, you're going to change all that by refactoring every frontend file applicable into a TypeScript file.


### 3.2 Testing

#### 3.1.1 Unit Testing
You will need to write unit tests for your component which displays the available products. This is to ensure that your component works the way you expect it to.

*Note: take a look into Jest*

#### 3.1.2 Usability Testing
You will need to write a simple usability test route that conforms to the following user actions:

1. Loading the website
2. Clicking the remove button (this will fail since there is no button as the admin hasn't been logged in yet)
3. Clicking the login button
4. Clicking the remove button of the first product on the list (this will pass since the admin is now logged in)
5. Clicking the logout button

*Note: take a look into Cypress*

***

<h2 id="assumptions">4. Assumptions 🤔</h2>
Here's some helpful assumptions that you can make about the project:

- You are allowed to use external component libraries.
- You are allowed to use different methods of styling (i.e. styled-components, tailwindcss, etc).

**You are not allowed to "get inspiration" from other applicant's code. We want to see your work, not someone else's. Nothing's stopping you from using someone else's code, but if you do, chances are that you will struggle when doing real dev work in Projects, and no one wants that.**

<h2 id="submission">5. Submission and Assessment 🏁</h2>

To make a submission, ensure that your forked repository is public and paste a link to it in your Projects Application in the relevant field. You will be assessed on the following aspects:
1. Code quality
2. Code style
3. Use of semantic tags
4. Use of meaningful class names and ids (where applicable)
5. Presentation of website
6. Functionality/Amount of tasks completed
7. Linting
8. TypeScript refactor (Extension)
9. Unit testing (Extension)
10. Usability tests (Extension)