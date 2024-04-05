# CI/CD Pipelines

## Environment
My CI/CD pipeline operates at a web level through the use of GitHub. Since it is integrated and deployed to a website instead of a download, the user's operating system does not matter as long as it can access the web.
The deployment is provided through GitHub's cloud and network, so cloud data is not a concern on the developer's side, but network configurations that blacklist web access are a concern in terms of making sure the deployed application can be seen.


## Tools
The tools used in the pipeline are GitHub Actions. GitHub Actions is used to automatically update and deploy the Flutter application to the website whenever new code is merged with the main branch.


## Automation Process
- Code Compilation: Flutter's dependencies are automatically installed by the instructions placed within the workflow file that GitHub Actions executes. These instructions also include "flutter build web", which primes the code for the web.
- Unit Testing:
- Integration Testing: 
- Deployment:


Your task is to draft the CI/CD pipeline section of your semester project report. Your draft should encompass the following components:

CI/CD Pipeline Environment:
Describe the infrastructure and environment where your CI/CD pipeline operates. Consider factors such as operating systems, cloud services, and network configurations.

CI/CD Pipeline Tools:
Identify and justify the selection of tools used in your CI/CD pipeline. Discuss their features, strengths, and limitations. Common tools include Jenkins, GitLab CI/CD, Travis CI, CircleCI, and GitHub Actions.

Automation Process:
Outline the process for automating the build and deployment phases of your CI/CD pipeline. Include steps for code compilation, unit testing, integration testing, and deployment to production or staging environments.
