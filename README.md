## Chordata - A Controlled Drug Register and Veterinary Practice Management Web Application

The goal of this project is to provide an easy to use, accessible, and secure web application that will allow veterinary practices to manage and track their controlled drugs, cremations, and dentals. The development of this application will make use of the Feature Driven Development methodology in each step of the development process from ideation up to and including project release.

The purpose behind the project is to reduce the need for physical storage of veterinary data by offering an electronic means of storage while also reducing the time veterinary professionals spend doing manual tasks that can easily be automated freeing up their time so they can do what they do best - caring for our pets.

## Installation Requirements

- Code editor of your choice
- [GIT](https://git-scm.com)
- [Node](https://nodejs.org/en/download/) - For npm
- [PostgreSQL & PSQL](https://www.postgresql.org/download/) - For the database

## Installation

Ensure you have all the installation requirements above before continuing with the installation

- Open a terminal instance in a directory of your choosing and run the following command to clone the repo `git clone https://github.com/c18742005/ChorData.git`
- The directory chosen will be referred to as ~/chosen-directory/ for the remainder of this document

### Installing Postgres and Setting up the Database

1. Download and install PostgreSQL and the PSQL command line tools using the official download [here](https://www.postgresql.org/download/) (Warning: System may need to be restarted to ensure correct installation)
2. Once installed, open a terminal and type the command `psql -U your-username` replacing your-username with the username used when setting up Postgres
3. To create the ChorData database type the command `CREATE DATABASE chordata;`
4. Enter the command `\l` and ensure the chordata database is listed. Press 'enter' to end the command
5. To connect to the database use the command `\c chordata`
6. Open the db.sql file located in the ~/chosen-directory/ChorData/chordata-backend directory in a code editor of your choice and copy its contents
7. In the open terminal instance, paste the copied contents from the step above, wait until the code has finished loading, and press 'Enter' to create the database
8. Open the .env file located in the ~/chosen-directory/ChorData/chordata-backend directory in a code editor of your choice (Warning: This file may be hidden by your OS by default. Ensure your hidden files are viewable in order to see this file)
9. Replace the DATABASE_URL variable using the following format: `postgres://username:password@localhost:5432/chordata` where username and password are the credentials you use to login to PSQL. If you did not set a password use `postgres://username@localhost:5432/chordata` instead where username is the username used to login to PSQL
10. Once the above instructions are completed, this terminal can be closed

### Installing Node and Setting up the Backend

1. Download and install NodeJS and NPM using the official documentation [here](https://nodejs.org/en/download/) (Warning: System may need to be restarted to ensure correct installation)
2. Once installed, open a new terminal instance and navigate to the ~/chosen-directory/ChorData/chordata-backend directory
3. Run `npm install` to install all required dependencies
4. (OPTIONAL) Run `npm test`. All tests should pass outlining successful setup of the backend
5. Once the above has finished, execute `npm run dev` in the terminal to run the development environment
6. Keep this terminal open and running for the duration of development

### Installing React and Setting up the Frontend

1. Open a new terminal and navigate to the ~/chosen-directory/ChorData/chordata-client directory
2. Run `npm install` to install the required dependencies
3. Run the command `npm run start:dev` to run the frontend in development mode
4. Open a browser and type in the url: `http://localhost:3000/`. This should navigate you to the login page. (After running the above command, a tab may be opened automatically for you)
5. Keep this terminal open and running for the duration of development
6. The following 2 accounts are set up to allow you to sample the system:

<b>Vet account</b>

- Username: vet.user
- Password: P@ssword1

<b>Nurse account</b>

- Username: nurse.user
- Password: ChorD@t@1

## How to use the deployed version?

The application is deployed using [Render](https://render.com)'s hosting services. The application can be accessed at the following link https://chordata.onrender.com

<b>To login as a vet:</b>

- Username: vet.user
- Password: P@ssword1

<b>To login as a nurse:</b>

- Username: nurse.user
- Password: ChorD@t@1

Features can be trialed and tested with the two above accounts. Alternatively new users can be created using one of the following Clinic ID's on the register page giving access to two separate example clinics:

- 292a485f-a56a-4938-8f1a-bbbbbbbbbbb1
- 292a485f-a56a-4938-8f1a-bbbbbbbbbbb2

## Code style

[![js-standard-style](https://img.shields.io/badge/code%20style-standard-brightgreen.svg?style=flat)](https://github.com/feross/standard)

## Tech/framework used

<b>Built with</b>

- [React](https://reactjs.org)
- [Node](https://nodejs.org/en/)
- [Express](https://expressjs.com)
- [GIT](https://git-scm.com)
- [Visual Studio Code](https://code.visualstudio.com)
- [PostgreSQL & PSQL](https://www.postgresql.org)
- [Render](https://render.com)
- [GitHub](https://github.com)
- [Jest](https://jestjs.io)
- [Figma](https://www.figma.com)

## Features

- Veterinary Controlled Drug Register
- Canine & Feline Dental Record Log
- X-ray Exposure Log
- Add/Edit/Deactivate Clients
- Add/Edit/Deactivate Patients
- View Patient Procedures

## License

MIT © [Steven Aherne](https://opensource.org/licenses/MIT)
