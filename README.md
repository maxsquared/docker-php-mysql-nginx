# docker-php-mysql-nginx

## Usage

### Installation

#### Step 1:

First install Docker

#### Step 2:

There are 2 ways to get PHP running.

##### Option 1

Download the folder by clicking on the **code** button, then **download zip**

Unzip docker-php-mysql-nginx

##### Option 2

Require git install on your computer, check if you have git installed, if not install git:
https://github.com/git-guides/install-git

Launch Terminal or CMD, CD into a directory where you usually keep your codes.

Clone this repository by using the command below:

```
git clone https://github.com/maxsquared/docker-php-mysql-nginx.git
```

### Launch PHP environment

Then anytime you need to run php just run the following command

```
cd docker-php-mysql-nginx
docker compose up
```

Wait for magic to happen

Make a directory in docker-php-mysql-nginx: **src** and put your php or project files in this direcotry, then you are good to go.

Use port **8080** for the website: _http://localhost:8080_

### To end the process

Go back to the terminal
Use control + c (Win/Mac)

### MySQL

Username: root

Password: **supersafepassword**

Password can be change in _docker-compose.yml_

When connecting to MySQL server ensure to use server name: **php_mysql_1**, localhost will not work.

### Optional Step - This will allow auto formatting for PHP on save

First install Node JS from this link: _https://nodejs.org/en/_

Install dev dependences by running the following command from

DOCKER-PHP-MYSQL-NGINX directory in your Terminal(Mac) or CMD(Windows): npm install

Once finished the step, restart Visual Studio code

PHP documents should now auto format whenever you save any changes.

#### Problems

If auto save doesn't work for you, follow step below:
Type CMD + SHIFT + P (Mac) or Control + Shift + P (Windows)
Find by typing: Preferences: Open settings (JSON) and select this option
Scroll to the end of the document, **before the closing curly (}) bracket** and paste in the following code:

```
"[php]": {
    "editor.defaultFormatter": "esbenp.prettier-vscode",
    "editor.insertSpaces": true,
    "editor.tabSize": 4
  },
```
