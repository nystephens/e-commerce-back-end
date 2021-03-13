# e-Commerce Back End Database

## Table of Contents
1. [Description](#description)
2. [Installation](#installation)
3. [Usage](#usage)
4. [License](#license)
5. [Contributing](#contributing)
6. [Tests](#tests)
7. [Questions](#questions)

## Description
This is a RESTful API to be used as a back end for an e-commerce website.  It is an Express.js API and is configured to use Sequelize to interact with a MySQL database.  A user is able to Create, Read, Update, and Delete (CRUD) entries in the database for products, categories of products, and associated product tags.  This information can be integrated fully into the front end of a shopping website or application so that these changes and requests can be made on the client side.  

## Installation
1.  Navigate to the GitHub repository ( https://github.com/nystephens/e-commerce-back-end ) in your web browser and click the green dropdown menu that says “Code”.  Copy the SSH key to your clipboard and then open your terminal.  

2.  In your terminal navigate to the directory you wish to house this repository.   

3.  Type “git clone” into your command line and paste the SSH key you copied from the repository, then hit Enter.  A new file titled “e-commerce-back-end” containing the necessary files will appear in your chosen directory.  Due to file size, Node.js and is necessary  modules will not be cloned to your repository. The ".env" file for this repository is also not included for privacy reasons.  You must create this file on your own. Please continue reading the instructions to find out how to install node modules on your computer and how to create a .env file.   

4.  Since this application uses Node.js you will have to install Node and the required Node modules to operate it.  For detailed instructions on how  to install Node.js to your computer please visit: https://www.guru99.com/download-install-node-js.html  

5.  Once Node is successfully installed on your computer, navigate to the index.js file in your terminal.  For quick access you can right click index.js in VS Code and click the option “Open in Integrated Terminal”. 

6.  Type the following command to install the proper node modules: “npm install”.  

7.  Check your newly downloaded “node_modules” folder to ensure that the correct packages have been installed.  The dependencies that are not included within the general Node module package are "dotenv”, "express", "mysql2", and "sequelize".  If these packages are not present within your Node modules then run the command “npm install dotenv express mysql2 sequelize” to install them.  

8.  To easily test the API and query for results you can use the application Insomnia Core.  Insomnia Core will allow you to easily create routes with the proper endpoints and test CRUD operations.  To download and install Insomnia Core visit [download Insomnia Core](https://insomnia.rest/download).

9.  Once you have cloned the repository, downloaded Node.js and its necessary modules, and installed Insomnia Core you are ready to use the e-Commerce Back End Database!  

## Usage
To use this API it is recommended to download Insomnia Core.  See [Installation](#installation) step 8 for instructions on how to download this application.  Once your Insomnia Core app is ready you must set up your database and seed the mock information.  Before you can run these commands you must create your .env file.  

Right click on your root directory and add "New File".  Name your new file ".env" and populate it with the following information: 

DB_NAME=ecommerce_db

DB_USER=\<your mysql username\>

DB_PW=\<your mysql password\>

Once your .env file is created you will be able to run the source command in mysql.  Log into mysql by entering the command "mysql -u \<your mysql username\> -p"  in  your terminal in the root directory.  Enter your password.  Once you are logged in run the command "source db/schema.sql".  When that is finished with no errors you can quit out of mysql by running the command "quit".

Now that your database and tables are created you can seed the database with the mock info provided in the seeds folder.  In the terminal while located in the root directory run the command "npm run seed".

After your database is seeded with information you are able to do your CRUD operations in Insomnia.  

For info on how to run these operations see [Using Insomnia](https://apis.support.brightcove.com/general/use-insomnia-api-requests.html).  When you run these different requests you should see the expected values for each request as defined by the models.

## License
![MIT license](https://img.shields.io/badge/license-MIT-brightgreen)
[MIT license](https://opensource.org/licenses/MIT)
Copyright <YEAR> <COPYRIGHT HOLDER>

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the "Software"), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.

## Contributing
If you would like to contribute to this project please contact me at the github link below.  I would love to expand this application and use it in various e-commerce settings by creating an interactive front end that brings the full experience of shopping online to users.  

## Tests
To test this application see the [Usage](#usage) section for details on how to preform CRUD operations in Insomnia Core.  By purposely entering incorrect values into your request you should recieve error messages corresponding to that request.  By entering valid information into your request body or url parameters you should recieve expected information corresponding with your request.  Trying different types of values within different CRUD operations should result in either and error or a valid result.  

## Questions
For questions or concerns regarding this project or future collaborations please contact the author via GitHub at:
https://github.com/nystephens
