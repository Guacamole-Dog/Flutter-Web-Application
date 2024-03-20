## Source Code Version Tools

### Introduction

Version control is an essential component in every form of software development because it allows developers to synchronize their code, isolate and fix bugs with minimal collateral, and cleanly track the history of changes to return to at any time.

The VCS I have chosen for my project was Git due to its low entry point, its capabilities, and its popularity among developers. Git is easy to get into, yet has a lot of features and integrations, and by learning to utilize Git, I will be prepared for when I use in future projects and jobs.

### Repository Setup
- My setup currently uses the main branch for whatever the user needs to download. Branches are made to safely merge in new changes but also to store files that are either optional add-ons or things that the main branch installs. The bulk of the code is contained within files within the branch, with things such as READMEs or launchers existing on the surface level.
- For my DevContainer, the Master branch essentially acts like the Main branch. For my CI/CD pipeline, since it installs files that don't need to be stored, only the Main branch is needed and no other branches are needed to store files.
- My commit messages are informal at the current moment, with simple descriptions of what the commits got done. Branches used for merging are temporarily named an arbitrary name that can be associated with my GitHub account (for when I collaborate with others), while branches used for file storage are given the name "Source" or "Files" and branches used for add-ons are either named after the specific add-on or given the blanket name "Extras". I have not had the opportunity to fully utilize these conventions, especially in this class, but they are what I still abide by.

### Common Commands and Usage
- Git init: 

### Collaboration Features

### Challenges/Solutions and Conclusion
