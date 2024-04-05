# CI/CD Pipelines

## Environment
My CI/CD pipeline operates at a web level through the use of GitHub. Since it is integrated and deployed to a website instead of a download, the user's operating system does not matter as long as it can access the web.
- **The deployment is provided through GitHub's cloud and network,** so cloud data is not a concern on the developer's side, but network configurations that blacklist web access are a concern in terms of making sure the deployed application can be seen.


## Tools
The tools used in the pipeline are GitHub Actions. GitHub Actions is used with custom workflow files to automatically update and deploy the Flutter application to the website whenever new code is merged with the main branch. 
- **GitHub Actions is very powerful due to its innate integration with GitHub, meaning that use of another program or service is not needed if the repository is within GitHub.** Additionally, GitHub provides a lot of pre-packaged tools to developers, making learning easier, and is very scalable.
- **However, GitHub Actions is dependent on GitHub and therefore has very limited third-party integrations.**


## Automation Process
- **Code Compilation:** Flutter's dependencies are automatically installed by the instructions placed within the workflow files that GitHub Actions execute. These instructions also include "flutter build web", which primes the code for the web.
- **Unit Testing:** Alongside "flutter test", additional unit tests are executed through packages provided by the internet. These tests are initially run through VS Code, but are then automated through additional workflow files after being confirmed to work.
- **Integration Testing:** Integration testing is not a concern due to the deployment being directed towards the web through GitHub, so testing for iOS and Android compatibility, for example, is not necessary. 
- **Deployment:** Once the code is compiled and the tests are complete, the GitHub Actions deploy the application to the web for the repository provided by GitHub.


