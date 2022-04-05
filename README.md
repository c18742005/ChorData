## Project title

The goal of this project is to provide an easy to use, accessible, and secure web application that will allow veterinary practices to manage and track their controlled drugs, cremations, and dentals. The development of this application will make use of the Feature Driven Development methodology in each step of the development process from ideation up to and including project release.

The purpose behind the project is to reduce the need for physical storage of veterinary data by offering an electronic means of storage while also reducing the time veterinary professionals spend doing manual tasks that can easily be automated freeing up their time so they can do what they do best - caring for our pets.

## Code style

[![js-standard-style](https://img.shields.io/badge/code%20style-standard-brightgreen.svg?style=flat)](https://github.com/feross/standard)

## Tech/framework used

<b>Built with</b>

- [React](https://reactjs.org)
- [Node](https://nodejs.org/en/)
- [Express](https://expressjs.com)
- [Visual Studio Code](https://code.visualstudio.com)
- [PostgreSQL & PSQL](https://www.postgresql.org)
- [Render](https://render.com)
- [Jest](https://jestjs.io)
- [Figma](https://www.figma.com)

## Features

- Veterinary Controlled Drug Register
- Canine & Feline Dental Record Log
- X-ray Exposure Log
- Add/Edit/Deactivate Clients
- Add/Edit/Deactivate Patients
- View Patient Procedures

## Installation Requirements

- [React](https://reactjs.org) - For the frontend
- [Node](https://nodejs.org/en/) - For npm
- [Express](https://expressjs.com) - For the backend API
- Code editor of your choice
- [PostgreSQL & PSQL](https://www.postgresql.org) - For the database

## Installation

Ensure you have all the installation requirements above before continuing with the installation

- Download the zipped folder from GitHub
- Unzip the downloaded file to a directory of your choosing (Referred to as ~/chosen-directory/ for the remainder of this document)

### Installing Postgres and Setting up the Database

1. Download and install PostgreSQL and the PSQL command line tools using the official download [here](https://www.postgresql.org/download/) (Warning: System may need to be restarted to ensure correct installation)
2. Once installed, open a terminal and type the command `psql -U your-username` replacing your-username with the username used when setting up Postgres
3. To create the ChorData database type the command `CREATE DATABASE chordata;`
4. Enter the command `\l` and ensure the chordata database is listed
5. To connect to the database use the command `\c chordata`
6. Open the db.sql file located in the ~/chosen-directory/ChorData-main/chordata-backend directory in a code editor of your choice and copy its contents
7. In the open terminal instance, paste the copied contents from the step above and press 'Enter' to create the database
8. Open the .env file located in the ~/chosen-directory/ChorData-main/chordata-backend directory in a code editor of your choice (Warning: This file may be hidden by your OS by default. Ensure your hidden files are viewable in order to see this file)
9. Replace the DATABASE_URL variable using the following format: `postgres://username:password@localhost:5432/chordata` where username and password are the credentials you used to login to PSQL

### Installing Node and Setting up the Backend

1. Download and install NodeJS and NPM using the official documentation [here](https://nodejs.org/en/download/) (Warning: System may need to be restarted to ensure correct installation)
2. Once installed, open a new terminal instance and navigate to the ~/chosen-directory/ChorData-main/chordata-backend directory
3. Run `npm install` to install all required dependencies
4. Once the above has finished, run `npm test` to test the setup so far and ensure it has been done correctly`
5. Once all tests have passed, run `npm run dev` to run the development environment
6. Keep this terminal open and running for the duration of development

### Installing React and Setting up the Frontend

1. Open a new terminal and navigate to the ~/chosen-directory/ChorData-main/chordata-client directory
2. Run `npm install` to install the required dependencies
3. Run the command `npm run start:dev` to run the frontend in development mode
4. Open a browser and type in the url: `http://localhost:3000/`. This should navigate you to the login page. (After running the above command, a tab may be opened automatically for you)
5. The following 2 accounts are set up to allow you to sample the system:

<bold>Vet account</bold>

- Username: vet.user
- Password: P@ssword1

<bold>Nurse account</bold>

- Username: nurse.user
- Password: vet.user

## Tests

- Follow the installation instructions above
- Open the chordata-backend directory `cd ~/chosen-directory/ChorData-main/chordata-backend`
- Run `npm test`
- All tests should pass outlining successful setup

## How to use?

To login as a vet:

- Username: vet.user
- Password: P@ssword1

To login as a nurse:

- Username: nurse.user
- Password: ChorD@t@1

Features can be trialed and tested with these two accounts

## License

MIT © [Steven Aherne](https://opensource.org/licenses/MIT)
