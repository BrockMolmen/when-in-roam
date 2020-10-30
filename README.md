# When In Roam

### About

A community-driven travel blog, where explorers can share their experiences, together. We encourage writers of all levels to share and grow while exploring the world. Whether it's your local coffee shop you stop by every morning or a bar you checked out while jet setting around the world, SHARE, GROW, EXPLORE!

### Development Approach

#### User Stories

* The user lands on a homepage where they can click on an "About" page to learn what the application is used for, select from "Regions" to see what others have posted, and sign up or log in.
* Once signed up and logged in, the user can create a new post by clicking on "New Post", go to their "Profile" page or click on "Regions" to explore posts from other users.
* "New Post" will direct them to a page to enter Region, Country, City, Location Type, Site Name, Date and Content, and then hit submit.
* Once user hits the "submit" button on their new post, the app will render their new entry and redirect them to their "Profile" page to see all of their own posts.
* On the user's profile page, users will be able to edit or delete any of their entries.
* With "Regions", users can select a specific region to explore all posts.

### Design Approach

#### ERD Database

We created a one-to-many Entity Relationship Diagram to help with our planning. One model for users and one model for posts that includes location and content information.

![ERD](./public/images/ERD.png)

#### Wireframes

These wireframes helped us to navigate and create routes and views and collectively design how we wanted our application to be used.

![wireframes](./public/images/wheninroamWireframes.png)

### Technologies

#### What it includes

* Sequelize user model / migration
* Settings for PostgreSQL
* Passport and passport-local for authentication
* Sessions to keep user logged in between pages
* Flash messages for errors and successes
* Passwords that are hashed with BCrypt
* EJS Templating and EJS Layouts

#### Default Routes

| Method | Path | Location | Purpose |
| ------ | ---------------- | -------------- | ------------------- |
| GET | / | server.js | Home page |
| GET | /auth/login | auth.js | Login form |
| GET | /auth/signup | auth.js | Signup form |
| POST | /auth/login | auth.js | Login user |
| POST | /auth/signup | auth.js | Creates User |
| GET | /auth/logout | auth.js | Removes session info |
| GET | /profile | server.js | Regular User Profile |

## Steps To Use

#### 1. Create a new repo on Github and use your 'express-authentication' as the template

When we are finished with this boilerplate, we are going to make it a template on Github that will allow us to create a new repo on Github with all this code already loaded in.
* Go to `github.com` and create a new repository. In the template dropdown, choose this template.
* Clone your new repo to your local machine
* Get Codin'!

#### 2. Delete any .keep files

The `.keep` files are there to maintain the file structure of the auth. If there is a folder that has nothing in it, git won't add it. The dev work around is to add a file to it that has nothing in it, just forces git to keep the folder so we can use it later.

#### 3. Install node modules from the package.json

```
npm install
```

(Or just `npm i` for short)

#### 4. Customize with new project name

Remove defaulty type stuff. Some areas to consider are:

* Title in `layout.ejs`
* Description/Repo Link in `package.json`
* Remove boilerplate's README content and replace with new project's readme

#### 5. Create a new database for the new project

Using the sequelize command line interface, you can create a new database from the terminal.

```
createdb <new_db_name>
```

#### 6. Update `config.json`

* Change the database name
* Other settings are likely okay, but check username, password, and dialect

#### 7. Check the models and migrations for relevance to your project's needs

For example, if your project requires a birthdate field, then don't add that in there. 

> When changing your models, update both the model and the migration.

#### 8. Run the migrations

```
sequelize db:migrate
```

#### 9. Add a `.env` file with the following fields:

* SESSION_SECRET: Can be any random string; usually a hash in production
* PORT: Usually 3000 or 8000

#### 10. Run server; make sure it works

```
nodemon
```

or

```
node index.js
```
