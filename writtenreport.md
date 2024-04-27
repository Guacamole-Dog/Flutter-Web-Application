Written Report: Your comprehensive report should include the following sections:
Introduction: Overview of CI/CD pipelines and their significance in modern software development.
DevContainer Environment:Details of the Docker container configuration used for Flutter development.
Source Code Version Control Tools: Description of the version control system utilized (e.g., Git), focusing on how the source code is managed and integrated with the CI/CD pipeline.
CI/CD Pipeline Environment: In-depth description of the CI/CD pipeline setup, including any utilized cloud services or local environments.
CI/CD Tools: Exploration of the CI/CD tools selected for the project (e.g., GitHub Actions, GitLab CI/CD, Jenkins), focusing on their configuration and their roles in automating the build, test, and deployment processes.
Deployment Environment:Overview of the deployment environment for the Flutter application (e.g., Firebase Hosting, AWS Amplify, GitHub Pages), detailing any necessary setup configurations.
Flutter Web Application:Discussion of the Flutter web application developed, including its functionality, testing, deployment via the CI/CD pipeline, and any encountered development or deployment challenges.
Conclusion: Reflection on the project, including lessons learned, challenges encountered, and potential improvements for the pipeline or application.

## Introduction
**CI/CD (Continuous Integration/Continuous Deployment) pipelines are loosely defined systems that have the ability to automatically integrate changes into and deploy a given application.** They are loosely defined in the sense that their function can be performed in a number of different ways *(from GitHub Actions to tests and protocols made from scratch)*, leading to varying degrees of success *(most notably quantified by code coverage)Z*, but as long as it allows for automatic integration of updates and deployment of software, it is a CI/CD pipeline. CI/CD pipelines are irreplaceably valuable in modern software development because they cut down on several tedious aspects of debugging new code contributions. **Developers can find out exactly which contributions caused errors and what parts of the contributions failed a given test with no back-and-forth between other developers, no confusing mixups, and no need for discovery, all while the working contributions are automatically integrated and pushed out to improve the software.**

## DevContainer Environment
The Docker container configuration used for Flutter development is set up in Visual Studio Code, taking advantage of the compatibility plugins that VS Code has with Flutter and Docker. It uses a Flutter image provided by VS Code along with additional permission-giving configurations to set the user up so that they can freely create files and use the terminal with the capabilities for Flutter application development. All the user needs is VS Code and Docker Desktop, in which the latter is a given for any DevContainer.

## Source Code Version Control Tools
The version control system utilized is Git, which organizes files into a repository with branches that can be merged, updated, cloned, and more. The source code is managed through pull requests and simple pushes, which both trigger automatic tests to check if the updated code has any newfound issues. Only the main branch is linked to the CI/CD with automatic tests so that other branches can be prepared for merging without immediately setting off alarms.

## CI/CD Pipeline Environment
The CI/CD pipeline is set up completely at the web and cloud level through the use of a GitHub repository, with no local environments used except for what each individual developer uses to edit and push their code into the repository. All testing and building is done through the use of GitHub Actions, a built-in component of every GitHub repository that allows for automatic code execution when actions such as pushing to the main branch occur, and the deployment is done through GitHub Pages, another built-in feature that hosts the deployed code or branch of choice on the web through a GitHub-affiliated domain.

The deployment is provided through GitHub's cloud and network, so cloud data is not a concern on the developer's side, but network configurations that blacklist web access are a concern in terms of making sure the deployed application can be seen.
