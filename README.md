# A very minimal subtheme - not opinions.

PRs merge to /develop
Option 1:
merging to /develop compiles and cleans up. merges to /deploy-staging.
Branch rules:
Allow forced pushes
  Specify who can force push 

To avoid conflicts in deploy:
### branch setup
1. checkout deploy
2. add css to .gitignore
3. git rm css
4. merge develop (which has css in .gitignore)
### build
1. composer check-platform-reqs
2. composer validate --no-check-all
3. composer install --prefer-dist --no-progress
4. npm install in theme folder
5. create css folder if necessary
6. compile css
### commit
1. remove css from .gitignore
2. commit css folder
3. push force (to deploy)
 