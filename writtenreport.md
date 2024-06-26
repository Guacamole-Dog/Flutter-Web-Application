# Written Report: CSC 325 Spring 2024

## Introduction
**CI/CD (Continuous Integration/Continuous Deployment) pipelines are loosely defined systems that have the ability to automatically integrate changes into and deploy a given application.** They are loosely defined in the sense that their function can be performed in a number of different ways *(from GitHub Actions to tests and protocols made from scratch)*, leading to varying degrees of success *(most notably quantified by code coverage)*, but as long as it allows for automatic integration of updates and deployment of software, it is a CI/CD pipeline. 
- CI/CD pipelines are irreplaceably valuable in modern software development because they cut down on several tedious aspects of debugging new code contributions. **Developers can find out exactly which contributions caused errors and what parts of the contributions failed a given test with no back-and-forth between other developers, no confusing mixups, and no need for discovery, all while the working contributions are automatically integrated and pushed out to improve the software.**

## DevContainer Environment
**The Docker container configuration used for Flutter development is set up in Visual Studio Code, taking advantage of the compatibility plugins that VS Code has with Flutter and Docker.** It uses a Flutter image provided by VS Code along with additional permission-giving configurations to set the user up so that they can freely create files and use the terminal with the capabilities for Flutter application development. 
- **All the user needs to utilize the DevContainer is VS Code and Docker Desktop**, and the latter is a given for any DevContainer.

## Source Code Version Control Tools
**The version control system utilized is Git, which organizes files into a repository with branches that can be merged, updated, cloned, and more.** 
- **The source code is managed through pull requests and simple pushes, which both trigger automatic tests to check if the updated code has any newfound issues.** Only the main branch is linked to the CI/CD with automatic tests so that other branches can be prepared for merging without immediately setting off alarms.

## CI/CD Pipeline Environment
**The CI/CD pipeline is set up completely at the web and cloud level through the use of a GitHub repository, with no local environments used except for what each individual developer uses to edit and push their code into the repository.**
- **All testing and building is done through the use of GitHub Actions, a built-in component of every GitHub repository that allows for automatic code execution when actions such as pushing to the main branch occur, and the deployment is done through GitHub Pages, another built-in feature that hosts the deployed code or branch of choice on the web through a GitHub-affiliated domain.**

## CI/CD Tools
**The main tool used in the project was GitHub Actions, although Jenkins was planned to be implemented.**
- **GitHub Actions allows for automatic code execution through the use of highly configurable workflow files that let the developer create strings of commands** *(or specialized actions provided by other developers)* **within the repository that execute in reaction to triggers of the developer's choice**, which allows for a facilitated build and deployment process within the CI/CD. 
- **Jenkins specializes in automated testing, allowing for most of the code in an application to have its performance thoroughly checked and documented for the developer to see.** It functions by being implemented through job configurations, which automatically perform their respective tests and provide output in an HTML that can be opened up by the developer. Since jobs can be placed in and executed through workflow files, **Jenkins has compatibility with GitHub through GitHub Actions, which makes for a smooth combo implementation in the CI/CD.**

## Deployment Environment
**The application is deployed entirely through GitHub Pages which, alongside being a built-in component of every GitHub repository, has direct compatibility with** *(or rather, reliance on)* **GitHub Actions.**
- **To set a repository up for GitHub Pages, the user must either choose a branch for GitHub to automatically deploy with or set up their own deployment with a custom workflow file that includes an action such as deploy-pages.**
- **In this application, a branch was chosen for GitHub to automatically deploy, but GitHub Actions was used to build web artifacts and automatically commit them to that chosen branch.** This is because, beyond a simple README or HTML file, using GitHub's built-in branch deployment requires extra building steps if it is to result in the application successfully running on the web.

## Flutter Web Application
**The original plan was to transfer a simple Flutter application that I created to be the app that this CI/CD helps with.** This Flutter application created randomly generated words and let the user mark their favorite words with a star to store them in a special tab. **However, the application that was implemented instead was a sample Flutter application that formed the skeleton for a basic adventure game.**
- Even after switching the application of choice to deploy, there were still issues with successfully having the Flutter application load on the website even after being built. *If I had put aside more time to work out that problem, it would likely have been fixed easily.* **The sample application can be tested through VS Code as long as Flutter is installed, but in terms of automated testing, all it has in its current state is a Smoke Test.**

## Conclusion
This project was a confusing adventure as it tread new ground at every step of the way, but I learned a valuable lesson: **When walking down a new path of knowledge, do not get complacent by early victories.** I did not put as much time as I should have into this project because I was surprised by how easily I was able to complete some of its early components, and I let the tangled late-game of the project sneak up on me and strike after I realized I had not given myself enough time. This is a *very* rookie mistake, one that I should not have made at this stage of experience.
- There are several improvements that could be made for the project, including implementation of Jenkins, improved functionality of the Flutter application *(or implementation of the originally planned application)*, cross-platform support for the DevContainer, increased code coverage through more tests, and... *getting the Flutter application to actually load properly on the website it is deployed to.*
