# SpoilerAlert

## Don't spoil it for me!

A project originally by the Pink Armadillo Fairies, iterated on by Team Velocirabbit.

## Team Velocirabbit Members
- Shun Ito   https://github.com/shundayo131
- Chris Nash   https://github.com/chrisnash819
- Colin Rooney   https://github.com/12mv2
- Kevin Sullivan   https://github.com/kevinsullivan88
- Justin Tran (Scrum Master)   https://github.com/justinvtran

## Special Thanks
We would like to thank Edwin Morlu for their invaluable advice to this project.

## Project Overview

SpoilerAlert is a web application built using React, Redux, and Express. It's an iteration on the original project found at https://github.com/Pink-Armadillo-Fairies/SpoilerAlert. The main focus of this iteration was to refactor and simplify the codebase.

## Vid walkthu of App

- A walkthru of the App is in client/assets

### Original Project Features
- Ability to comment on shows with friends without seeing spoilers for unwatched episodes
- Included one static show, Bridgerton
- Allowed adding comments to episodes and viewing comments up to the current episode

### Our MVP Enhancements
- Added ability to add new shows to the database
- Implemented a search show feature using an external API to fetch show, season, and episode data
- Allowed users to save and view a collection of shows they're watching in a dashboard
- Implemented login functionality using bcrypt and cookie-based session management
- Filtered the chat page to only show comments for a specific show
- Added dark mode feature
- Added styling

## Key Technologies
- Frontend: React, Redux, Bootstrap
- Backend: Express, Supabase/PostgreSQL

## Main Dependencies

- @reduxjs/toolkit
- bcryptjs
- bootstrap
- cookie-parser
- dotenv
- express
- googleapis
- html-webpack-plugin
- pg-promise
- react
- react-bootstrap
- react-dom
- react-redux
- react-router-dom
- redux
- sass
- sqlstring
- webpack

## Setup and Installation

1. Clone the repository:
git clone [Your repository URL]
cd [Your project directory]
Copy
2. Install dependencies:
npm install
Copy
3. Set up environment variables:
Create a `.env` file in the root directory and add the following: ()
SUPABASE_PG_KEY="your-supabase-postgres-password"
SUPABASE_API_KEY="your-supabase-api-key"

To obtain these keys:
- Log in to your Supabase account and create a new project
- Go to Project Settings > Database to find your Postgres password
- In the API section, you'll find your project URL and API key
- Make sure to use the "anon" public API key for client-side access

4. Set up your Supabase database:
- In the Supabase dashboard, go to the SQL Editor
- Create necessary tables for users, shows, comments, etc.
- You can use the provided schema in the `db_schema.sql` file (if available)
- In db_config.js use your Supabase url: SUPABASE_PROJECT_URL="your-supabase-project-url"

5. Start the development server:
npm run dev
CopyThis command runs both the frontend and backend in development mode.

## Usage

- For development:
- `npm run dev`: Starts both frontend and backend in development mode
- Frontend runs on `localhost:8080`
- Backend runs on `localhost:3000`

- For production:
- `npm run build`: Builds the production version
- `npm start`: Starts the production server

## Scripts

- `build`: `NODE_ENV=production webpack`
- `start`: `NODE_ENV=production nodemon server/server.js`
- `dev`: `concurrently "NODE_ENV=development webpack serve --open" "NODE_ENV=development nodemon server/server.js"`

## API Routes

The server provides the following main routes:

- GET `/`: Serves the main application
- GET `/searchshows`: Search for shows and create them in the database
- GET `/getshow`: Retrieve show information from the database
- POST `/saveplace`: Save the season/episode a user is on
- GET `/getwatchhistory`: Retrieve a user's watch history
- POST `/saveusershow`: Save a show for a user
- GET `/getcomments`: Retrieve comments for a show
- POST `/addcomment`: Add a comment to a show
- POST `/users/login`: User login
- POST `/users/signup`: User signup
- GET `/shows`: Retrieve shows saved by a user

## Project Structure
.
├── LICENSE
├── README.md
├── tests
│   └── server-tests
│       ├── getcomments.test.js
│       └── searchshow.test.js
├── build
│   ├── bundle.js
│   ├── bundle.js.LICENSE.txt
│   └── index.html
├── client
│   ├── Headers.css
│   ├── assets
│   │   ├── bridgerton.jpg
│   │   └── supermario.jpg
│   ├── components
│   │   ├── AddShow.jsx
│   │   ├── App.jsx
│   │   ├── Comment.jsx
│   │   ├── DarkModeToggle.jsx
│   │   ├── Dashboard.jsx
│   │   ├── Header.jsx
│   │   ├── LoginForm.jsx
│   │   ├── MainPage.jsx
│   │   ├── Show.jsx
│   │   ├── Signup.jsx
│   │   └── WatchParty.jsx
│   ├── episodeSlice.js
│   ├── loginSlice.js
│   ├── main.js
│   ├── store.js
│   └── styles.css
├── index.html
├── package-lock.json
├── package.json
├── server
│   ├── commentController.js
│   ├── controllers
│   │   ├── commentController.js
│   │   ├── cookieController.js
│   │   ├── sessionController.js
│   │   └── userController.js
│   ├── controllers.js
│   ├── db_config.js
│   ├── episodeController.js
│   ├── seasonController.js
│   ├── server.js
│   └── showController.js
└── webpack.config.js
Copy

## Notes for Developers

### Current Bugs and Known Issues
- [List any known bugs or issues here]

### Future Enhancements
- [List any planned or suggested future enhancements]

### Important FYIs
- Make sure to never commit your .env file to version control. Add it to your .gitignore file to prevent accidental commits.
- [Any other important information for developers]

## Using the code / repo

Please clone and use SpoilerAlert! 

