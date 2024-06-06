# Week3-CI-Activity: Instructions

This repository contains a basic implementation of a calcular, similar to the one you developed during the TDD class activity.

In today's class activity we'll create a basic CI workflow. To do so, please follow the steps below.

1. Install and build the project, and confirm that the tests work:
```
npm install
npm run build
npm run test
```

2. Create a directory `.github` with a subdirectory `.github/workflows`

3. Now, your task is to create a file `.github/workflows/ci.yml` that will contain your workflow. This workflow must satisfy the following requirements:
* Runs on every commit to the main branch
* Runs on every pull request to the main branch
* Runs when manually started by the user
* Installs required OS package dependencies and npm dependencies
* Runs all tests

Please do not copy the sample YAML from the slides. It is for demonstration
purposes and may not work for you! You will have to write this by hand.

4. Once you have written your .yml file, `git add` it, `git commit` it, and `git push` it. Your Actions should kick off automatically.

Hint: you may find it helpful to do this in stages. Try writing an Action that just prints "hello world" first, for example. Then try adding code that checks out the project, then add code that builds the code, then adding code that runs the tests.

5. Your final task is to experiment with some of the advanced features that are available with GitHub Actions. Please consult the documentation at `https://docs.github.com/en/actions` and try out a few of them. Examples of things you can try are:
* triggering an action when a new issue is created
* creating a ZIP file artifact containing the output of running the tests so that it can be downloaded from the GitHub actions page
* scheduling a periodic run of your tests (if you try this, please be sure to remove it after submitting your class activity to avoid wasting compute resources)

## Submitting
Submit your CI file (.github/workflows/ci.yml), a screenshot of your
passing GitHub actions run, and a README via GradeScope. In the README, please include:
* The names of everyone who was involved in this activity
* The singular GitHub repo of one group member that you are submitting for grading
Please also include all group member names in the GradeScope submission itself.