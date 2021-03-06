# E-Commerce Back-End

## User Story

```md
AS A manager at an internet retail company
I WANT a back end for my e-commerce website that uses the latest technologies
SO THAT my company can compete with other e-commerce companies
```

## Table of Contents

- [Preview](#Preview)
- [Walkthrough](#walkthrough)
- [Installation](#Installation)
- [Database Schema](#Database-Schema)
- [Tests](#Tests)
- [Documentation](#Documentation)
- [Feedback](#Feedback)

---

## Preview

Here is how the application appears and functions in Insomnia

<img src='images\insomnia-preview.gif' />

## Walkthrough

This video will show you how to set up the project.

- [Project Set-Up](https://youtu.be/QH67snvhrUM)

The following videos show the routes being tested in Insomnia.

- [Part One](https://youtu.be/32ZebCXC6ng)
- [Part Two](https://youtu.be/EtpS9fMYTZs)

## Installation

_This project requires Node.js and other dependencies_

- [How to install Node](https://docs.npmjs.com/downloading-and-installing-node-js-and-npm)

After you have installed Node, navigate to the directory you would like to use using the CLI and then clone this repository:

```bash
git clone git@github.com:wolfskillobyte/black-friday.git
```

Create `.gitignore` to include the following:

```bash
node_modules
.env
.DS_Store
package-lock.json
```

`.env` will hold your sensitive information.

```bash
DB_NAME='ecommerce_db'
DB_USER='root'
DB_PW='YOUR_PASSWORD_HERE'
```

Open VS code and use these commands to get you started:

```bash
npm install mysql2 dotenv express sequelize
npm init
```

`npm init` will create your `package.json` file.
Make sure `package.json` includes the seed in your scripts:

```json
"scripts": {
    "test": "echo \"Error: no test specified\" && exit 1",
    "start": "node server.js",
    "seed": "node seeds/index.js"
}
```

Login to MySQL with your credentials. 
```bash
mysql -u root -p
```
In the MySQL terminal, start the database
```mysql
USE ecommerce_db;
```
Then seed the schema files
```mysql
source ./db/schema.sql;
```

Go back to your main terminal or VS Code powershell and enter 
```bash
npm run seed
``` 
This will seed all the files so they can be tested in Insomnia.

Finally, start the application from the command line:

```bash
node server
_OR_
npm start
```

## Database Schema

<img src='images\db-schema.png' />

## Tests

_This project used Insomnia for testing_

<a href="https://docs.insomnia.rest/">
  <img src="https://img.shields.io/badge/Insomnia-black?style=for-the-badge&logo=insomnia&logoColor=5849BE" />
</a>

## Documentation

- [npm](https://docs.npmjs.com/)
- [MySQL2](https://www.npmjs.com/package/mysql2)
- [Express](https://expressjs.com/en/4x/api.html)
- [Sequelize](https://sequelize.org/master/)

## Feedback

Have something you'd like to add?<br>
Feel free to contact me via email!<br>

<a href="mailto:sraewolfskill@gmail.com">
  <img src="https://img.shields.io/badge/Gmail-D14836?style=for-the-badge&logo=gmail&logoColor=white" />
 </a>
