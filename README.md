My execution is that I put every file in the same branch, since the Github Actions pull from Flutter anyways. The Actions check for all the Flutter dependencies before copying over the Flutter web application and building it.

My challenges were figuring out how to launch the workflow. I ended up having it occur on push to get it to work.


## For the user
To install Flutter dependencies, open VS Code and install the Flutter extension, which will automatically grab the SDK on any folder that doesn't have one.
