- [ ] **how to set up travis**
- Visit: https://travis-ci.com/ and click "Sign in with GitHub".
- Accept the Authorization of Travis CI. You’ll be redirected to GitHub.
- Choose the repository you want to run Travis CI on and activate it.
- Add a *.travis.yml* file to your repository to tell Travis CI what to do.
- Tell Travis CI which language and version you are running..
   ```
   language: node_js
   node_js:
   - "node"
   ```
- Add the *.travis.yml* file to git, commit and push, to trigger a Travis CI build.

  - [ ] **How to make travis run your tests**
   - In the package.json file there's a scripts element, where you can specify the *test command*, 
   which Travis will look for and run!
   ```
   "scripts": {
    "test": "tape test.js | tap-spec"
  }
   ```
   
  - [ ] **How to make travis run something else (eg a linting script)**
   - As Travis looks only for the *test command*, you can run the other commands you want through
   the *test command* itself as following:
   ```
    "scripts": {
    "lint": "./node_modules/.bin/eslint test.js",
    "test": "npm run lint & tape test.js | tap-spec"
  }
   ```
   
  - [ ] **Bonus hard check how to make travis build it’s own database for testing on…**
   - Start PostgreSQL in your .travis.yml:
   ```
   services:
  - postgresql
   ```

   - Create a database for your application by adding the foloowing line to your .travis.yml:
    ```
    before_script:
    - psql -c 'create database travis_ci_test;' -U postgres
    ```
  - The default user for accessing the local PostgreSQL server is **postgres** with **a blank password**.
  
    *"so you need to add EV to Travis with the database url.."*
   ```
   DB_URL = postgres://postgres:@localhost:5432/travis_ci_test
   ```
  
- [ ] **How to set your app up on heroku**
  - [ ] **If your app heroku deploy doesn’t work, what can you do to find out the problem**
  - [ ] **How do you provision a database on heroku**
  - [ ] **How do you add environment variables on heroku**
- [ ] **What should we store in config.env file? Why?**
  - [ ] **Do the variable values in my config.env file have to be the same as their values on heroku?**
