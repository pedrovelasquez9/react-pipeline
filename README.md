## Tutorial link

[Go to video](https://www.youtube.com/watch?v=e3SV6tYztz0)

## Steps followed

- Create app react+typescript: **npm create vite@latest github-pipeline --template react-ts**
- Install deps:
  - **npm i**
  - **npm i gh-pages --save-dev**
  - **npm i react-router-dom**
- Add predeploy and deploy commands to package.json
  - "predeploy":"npm run build"
  - "deploy":"gh-pages -d dist"
- Edit build command:
  - "build": "tsc && vite build --base=/react-pipeline/"
- Test Github pages deploy
  - **npm run deploy**
- Create workflow file and folders for Github Actions:
  - code .github/workflows/build-deploy.yml
- Workflow useful links:
  - checkout action: https://github.com/actions/checkout
  - deploy action: https://github.com/JamesIves/github-pages-deploy-action
- Test integration with git push to master branch
