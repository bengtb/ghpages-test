 # ghpages-test

This is a small test of ghpages and React. It's actually so small you can't make it much smaller. Though it's not really much of an application.

You can see the result at [this link to gh-pages](https://bengtb.github.io/ghpages-test/)

## the steps

1. Create the repository on github.com

2. Go to `settings` at the top of the repo and choose `Pages` on the left.

3. Get yourself a private token if you don't already have one by going the your user's settings / Developer settings / Personal access tokens. Make a note of you token and add it to your password manager and not in the repo itself.

3. Make sure the gh-pages are on the `gh-pages`-branch

4. Create you small React based program.

5. Edit `package.json` and add this line at the top level:  

```json
   "homepage": "https://bengtb.github.io/ghpages-test"
```
and under `scripts` add these two lines:  

```json
    "predeploy": "yarn build",
    "deploy": "gh-pages -d build",
```

6. The repository's main branch and the gh-pages branch are totally separated.

7. Check in the source code to the repo so you don't loose it

8. Build the deployable compressed version of your application and deploy it:   
```bash
yarn deploy
```

9. Now check out the application at [this link to gh-pages](https://bengtb.github.io/ghpages-test/).