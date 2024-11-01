## Will a Capital Bikeshare bike be ready when you are?

Capital Bikeshare publishes its ridesharing data as part of its agreement to operate in the District of Columbia and its surrounding suburbs. Can we use the data to reliable predict when and where bikes or bike docks will be available?

## Docker

We all work from different computers, but this application needs to run locally on any computer. Docker makes that possible.

### For macOS after Catalina, or after than 10.15:

1. Install Homebrew, a package manager, using: https://brew.sh/
2. Open the Terminal application and run `brew install --cask docker.rb`
3. Try `docker run hello-world`. If you don't have this image locally, Docker will fetch it for you. Your terminal should output a message saying "This message shows that your installation appears to be working correctly."

### For macOS Catalina or lower, or prior to 10.15:

4. You can get an older version of Docker using the methods outlined in this post: https://stackoverflow.com/a/75132333/5057333
6. Get an older Docker version's brew cask and output it in your current directory: `curl https://raw.githubusercontent.com/Homebrew/homebrew-cask/1a83f3469ab57b01c0312aa70503058f7a27bd1d/Casks/docker.rb -O`
7. Try `brew install --cask docker.rb` again.
8. Run `docker run hello-world`
9. If you get the error -bash: docker: command not found, you can try what's recommended here to create some necessary files: https://stackoverflow.com/a/43365425/5057333
10. `Press ⌘ + Space to bring up Spotlight Search and enter Docker to launch Docker.` Follow the prompts to allow docker to create some necessary files.
11. Try `docker run hello-world` again. If you don't have this image locally, Docker will fetch it for you. Your terminal should output a message saying "This message shows that your installation appears to be working correctly."
16. Exit the container with `exit`.

17. 
18. Navigate the the repository with the desired dockerfile.
19. Run `docker build -t sandbox:bike-check-historical-database .`
20. Docker creates an <b>image</b> with the name sandbox:bike-check-historical-database in the current directory.
21. Have a coffee. This can take a while.
22. Run an interactive Docker container (i.e., one you can enter commands against) based on the image you just created with `docker run -it sandbox:bike-check-historical-database`
23. Check that the version of Python is what you expect (e.g., 3.11.6) by running `python`
24. Run `quit()` to leave the Python interpreter.
25. Exit all containers with `docker stop $(docker ps -a -q)`
