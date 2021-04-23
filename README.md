# Web 101 temp 8-Week Ebook

A dead simple Node Express app that serves static [Material Themed docs](https://squidfunk.github.io/mkdocs-material/) generated by [Mkdocs](https://www.mkdocs.org/) from behind basic authentication.

## For Development

1. Clone this repo
2. Install Node dependencies: `npm i` (see `package.json`)
3. Run `npm start` to see the current state of the ebook.
4. Start with `ebook-folder/mkdocs.yml` this is the configuration file for this book

## Install Python Dependencies

To be able to edit the ebook you will need to follow these steps first:

1. Install Python 3.7+ on to your computer
2. Install [pip](https://pip.pypa.io/en/stable/installing/)
3. `cd ebook-folder` to move into the Python package
4. run `git clone https://github.com/squidfunk/mkdocs-material.git`
5. Install the Python Packages `pip install -r requirements.txt` (See `requirements.txt`)
6. Run `mkdocs build` to build the markdown files into static HTML files into the `site/` directory.

## Serve

To serve the files in `site/` to port 8000 **withOUT** `username:password` authentication simply run `mkdocs serve`.

To serve **with authentication** you'll need to add `.env` file with environment variables to the root directory:

1. `cd ..`
2. `echo "STUDENT_USERNAME=a-username STUDENT_PASSWORD=a-password INSTRUCTOR_USERNAME=a-username INSTRUCTOR_PASSWORD=a-password PORT=5500" >> .env`
  
  ```txt
    STUDENT_USERNAME=a-username
    STUDENT_PASSWORD=a-password
    INSTRUCTOR_USERNAME=a-username
    INSTRUCTOR_PASSWORD=a-password
    PORT=5500
  ```

3. From `ebook-folder` run `mkdocs serve`
4. From root directory run `npm start` - to serve files from `site/` to port 5500 **with** username:password authentication

  > Go to `ebook-folder/mkdocs.yml` for further instructions + see `ebook-folder/workspace` for templates and notes.

  > While working in `ebook-folder/` you can simply use `mkdocs build` and `mkdocs serve` to by-pass the Node server.

## To Deploy

1. Finish your changes and check them with `mkdocs serve`.
2. Before you `git add` anything to staging run `mkdocs build`. This will ensure you've built the newest *intended* version of the ebook before you push it to GitHub.
3. `git status, add, commit, push ...` to repo
4. Create pull request & merge

## For New Deployments

Heroku will need some environment variables to perform authentication checks. Add them as you would the variables in `.env` file using [he CLI tools or the dashboard](https://devcenter.heroku.com/articles/config-vars).

* `ENVIRONMENT` : `PRODUCTION`
*  `STUDENT_USERNAME` : `<a-username>`
*  `STUDENT_PASSWORD` : `<a-password>`
*  `INSTRUCTOR_USERNAME` : `<a-username>`
*  `INSTRUCTOR_PASSWORD` : `<a-password>`

How to install Python and pip instructions here:

## Functional Overview

[Mkdocs](https://www.mkdocs.org/) is a Python package that generates statics web files (HTML, CSS, JS), seen in the `site/` directory, from plain Markdown files, seen in the `docs/` directory.

[Material-Mkdocs](https://squidfunk.github.io/mkdocs-material/) is another Python package that builds on top of Mkdocs to provide design from the Material-UI Theme. The two receive their configuration from the `mkdocs.yaml` file. You'll see the navigation is is provided by the `nav:` property in that file and the Material Theme is the value of `theme:`.

The [Express server](https://expressjs.com/) is just an app used to serve the static files from `site/` behind basic authentication thus the Node app is deployed and not the Python code.