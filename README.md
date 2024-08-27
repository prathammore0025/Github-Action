# CI/CD Pipeline Documentation

## Workflow Description

This GitHub Actions workflow automates the build and deployment process. It is designed to improve efficiency by ensuring that the project is built and deployed seamlessly with each update. The workflow is triggered by pull requests to the dev branch and by manual dispatch, ensuring that all changes are tested and deployed automatically.

## Workflow Overview
# Trigger Events:

The workflow is triggered by a push to the main branch.
It can also be manually triggered using workflow_dispatch.
Permissions:

The workflow is configured to have write permissions to the repository contents, allowing it to push changes to the gh-pages branch.

## Workflow Steps
# Clone Repository:
The workflow starts by cloning the repository to the GitHub runner. This step ensures that the latest codebase is available for building.

# Setup Node.js:
Node.js is set up with version 18 to provide the environment required for building the Cocos WebGL project.

# Install Dependencies:
The workflow runs npm install to install all necessary dependencies as specified in the package.json file.

# Build Project:
The project is built using the command npm run build. This step compiles the project into deployable artifacts.

# Deploy to GitHub Pages:
The built project is deployed to the gh-pages branch using the github-pages-deploy-action. This action handles the deployment of the build output to GitHub Pages, making the project accessible via a web link.
