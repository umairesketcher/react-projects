# Lula Store Platform Backend

### Tools Required:

NPM Package Manager, Node, Commitizen, Postgres Database

### Setup

1. Clone the project using `git clone https://github.com/Lula-Inc/lula-store-platform-backend.git`
2. Create .env file at root directory of project and Set the enviroment variables as writen in .env.example file.
3. Setup Database with DB creadantials.
4. goto src folder, then run the migrations with `npx sequelize-cli db:migrate`
5. goto src/script/update folder, then run all the script using `node <Script Name>`
6. Open the terminal at the root directory of the project and run the command `npm install` to install dependancies and required packages for the project.
7. now run the Server using `npm start`


### How to make and run migration:

1. Make migration using `npx sequelize-cli migration:create --name <Migration Name>`
2. Run Migrations using `npx sequelize-cli db:migrate`

### Project Structure

```
lula-store-platform-backend
┣ logs
┃ ┗ server.log                                        # Contains Error and Info Logs..
┣ src
┃ ┣ classes						# Contains all classes that ere used in controller.
┃ ┣ config						# Contains configration of Database, Handle bars and jwt passport
┃ ┣ controllers					# Contains logic of Handling incoming requests and returning responses.
┃ ┣ enums   						# Contains the enums used in the app.
┃ ┣ globals						# Contains Constants variables.
┃ ┣ helpers   						# Contains Helper Functions that are used in Controller to perform sub tasks.
┃ ┣ lib							# contains JWT creation code.
┃ ┣ middlewares					# Contains Authentications and Validation Middlewares.
┃ ┣ migrations  					# Contains Database DB Migrations.
┃ ┣ models  						# Contains All DB models
┃ ┣ public  						
┃ ┣ routes  						# Contains all the routes and routing logic for the app.
┃ ┣ scripts
┃ ┃ ┗ update						# Contains All scripts that populates Data in DB.
┃ ┣ serializer  					# Format response of Reports Data.
┃ ┣ views						# Contains email templates.
┃ ┣ app.js
┃ ┣ server.js
┃ ┗sheduled-jobs.js					# Contains All Cron job.
┣ test 						# Contains Test Scripts.
┣ .gitignore
┣ ecosystem.config.js
┣ nodemon.json
┗ package.json
```

