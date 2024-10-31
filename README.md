# bike-check
Will a Capital Bikeshare bike be ready when you are?

# Run the Docker Container

We all work from different computers, but this application needs to run locally on any computer.

Docker makes that possible.

# For macOS:

1. Install Homebrew, a package manager, using: https://brew.sh/
2. Open the Terminal application and run `brew install --cask docker.rb`
3. If your macOS is too old for the latest version of Docker, e.g., Catalina, you can get an older version per this post: https://stackoverflow.com/a/75132333/5057333
4. Get an older Docker version's brew cask and output it in your current directory: `curl https://raw.githubusercontent.com/Homebrew/homebrew-cask/1a83f3469ab57b01c0312aa70503058f7a27bd1d/Casks/docker.rb -O`
5. Try `brew install --cask docker.rb` again.
6. Run `docker run hello-world`
7. If you get the error -bash: docker: command not found, you can try what's recommended here to create some necessary files: https://stackoverflow.com/a/43365425/5057333
8. `Press ⌘ + Space to bring up Spotlight Search and enter Docker to launch Docker.` Follow the prompts to allow docker to create some necessary files.
9. Try `docker run hello-world` again. If you don't have this image locally, Docker will fetch it for you.
10. 
11. If you get an error referencing the docker daemon, check for existing docker images (you may not have any): `docker image ls`
12. There are deprecated CLI tools like docker-machine that you can use in conjunction with virtualbox to run docker...
13. But it's easier (and not deprecated) to start docker with `open --hide --background -a Docker` or just `open -a Docker`
14. If you're still seeing references to 
15. Now test that Docker is working by running `docker run hello-world`
16. Exit the container with `exit`
17. Navigate the the repository with the desired dockerfile
18. Run `docker build -t sandbox:bike-check-historical-database .`
19. Docker creates an <b>image</b> with the name sandbox:bike-check-historical-database in the current directory.
20. Have a coffee. This can take a while.
21. Run an interactive Docker container (i.e., one you can enter commands against) based on the image you just created with `docker run -it sandbox:bike-check-historical-database`
22. Check that the version of Python is what you expect (e.g., 3.11.6) by running `python`
23. Run `quit()` to leave the Python interpreter.
24. Exit all containers with `docker stop $(docker ps -a -q)`
