

# ===[ How to deploy to heroku ]===

## create the Node project
- Create and test Node.js Project 
 

## Set GitHub Repo
- Set Git & GitHub


## Create & Update files for Heroku

  ==> Create: 'Procfile'  
  - More info on how tocreate file: https://devcenter.heroku.com/articles/procfile
  - Code in file:    
      web: node index.js

  ==> Create: 'App.json'  
  - More info on how tocreate file: https://devcenter.heroku.com/articles/app-json-schema
  - Code in file:    
      {
        "name": "Start on Heroku: Node.js",
        "description": "Test Node app",
        "repository": "https://github.com/Edxael/01-Node-hk-cd",
        "logo": "https://cdn.rawgit.com/heroku/node-js-getting-started/master/public/node.svg",
        "keywords": ["node", "express", "heroku"],
        "image": "heroku/nodejs"
      }

  ==> Update: 'pakage.json'  
  - More info on how tocreate file: https://devcenter.heroku.com/articles/app-json-schema
  - Code in file: 
      Add the following categories:

    "engines": {
      "node": "8.15.0"
    },
    "repository": {
      "type": "git",
      "url": "https://github.com/Edxael/01-Node-hk-cd"
    },

  ==> Update: 'server.js' 
  - use the port on .env by: 
      app.listen((process.env.PORT || 5000), (err) => { ....

  ==> In my case I use the Build-Directory content for this reason I need to tell heroku to build it by adding the next script:
      "scripts": {
          .....
          "heroku-postbuild": "npm run build"
      }



## Install Heroku-CLI
- More info on: https://devcenter.heroku.com/articles/getting-started-with-nodejs#set-up
    (There is a Snap:  $ sudo snap install heroku --classic )

- Log-In: heroku login 

## Create the app: 
- More info on: https://devcenter.heroku.com/articles/getting-started-with-nodejs
- Follow the quck tutorial 

