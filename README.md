# Lab: Node Ecosystem, CI, CD

## Links

- [Pull request #1](https://github.com/dcalhoun286/server-deployment-practice/pull/1)
- [Pull request #2](https://github.com/dcalhoun286/server-deployment-practice/pull/2)
- [Deployed site](https://dc-server-deploy-prod.herokuapp.com/)
- [GitHub Actions](https://github.com/dcalhoun286/server-deployment-practice/actions)

## The Setup

### Github

1. Create a new repository at GitHub, called `server-deployment-practice`
  1. Select the "Add a README" option
  1. Select the "Add a .gitignore" option, and choose Node.js
  1. Opt for the MIT license
1. Clone this repository to your local machine.
1. Create a "dev" branch to do your work in: `git checkout -b dev`

### Heroku

1. Login to your Heroku account
1. Create a new Heroku app, called `yourname-server-deploy-dev`
  1. Go to the deployment tab
  1. Choose "GitHub"
  1. Connect to your repository
  1. Choose the "dev" branch
  1. Choose the "Wait for CI to pass before deploy" option
  1. Choose the "enable automatic deploys" option
1. Create a new Heroku app, called `yourname-server-deploy-prod`
  1. repeat all of the directions in step 2, but choose the "main" branch instead.

### The Code

1. Initialize your app: `npm init -y`
1. Install your dpeendencies: `npm i dotenv express jest supertest`
1. Create the files and folders required for the application
1. Create the correct content in the files
1. Test your server: `npm test`
  1. You should see 100% of tests passing
1. Start your server: `nodemon`
  1. Visit [http://localhost:3000/data](http://localhost:3000/data) in your browser to confirm that the server is visible

## Deploy

Now that you have it all running, let's get it deployed.

### First: Deploy to Dev

1. Complete an **ACP** on your `dev` branch.
1. Go immediately to the repository on GitHub and open the actions tab
  1. You should see  your tests running
  1. If they were passing on  your local machine, they'll also pass here
1. Once your tests have passed, go to Heroku.com and look at your dev app's **Activity** tab, it should hsow you have active deployment
1. When it completes, go to the Heroku app URL and open your server in the browser, you should see the same results as your saw locally.

### Second, go to production

Once your dev run has completed, you have successfully deployed your applicaiton through GitHub, with tests to an app on Heroku.

#### Now, we're going to complete the "real" deployment process

1. Go to your repository on GitHub
1. Open a pull request from `dev` to `main`
1. If your tests are passing, you will be able to merge this branch
1. Once you merge, the tets will run again using GitHub actions
1. Once the tests pass, Heroku will deploy your "main" branch to your "production" app!
1. When that process completes, open your app in the browser to prove it.

## Resources

1. I used this demo constructed by my instructor during class to complete this assignment
  1. [Class Demo](https://github.com/codefellows/seattle-javascript-401n18/tree/main/class-01b/demo/server)