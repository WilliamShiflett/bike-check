# bike-check
Will a Capital Bikeshare bike be ready when you are?

# Run the Docker Container

We all work from different computers, but this application needs to run locally on any computer.

Docker makes that possible.

# For macOS:

1. Install Homebrew, a package manager: https://brew.sh/
2. Open the Terminal application and run `brew install docker docker-compose`
3. Run `docker run hello-world`
4. If you get an error referencing the docker daemon, check for existing docker images (you may not have any): `docker image ls`
5. There are deprecated CLI tools like docker-machine that you can use in conjunction with virtualbox to run docker...
6. But it's easier (and not deprecated) to start docker with `open --hide --background -a Docker` or just `open -a Docker`
7. Now test that Docker is working by running `docker run hello-world`
8. Exit the container with `exit`
9. Navigate the the repository with the desired dockerfile
10. Run `docker build -t sandbox:bike-check-historical-database .`
11. Docker creates an <b>image</b> with the name sandbox:bike-check-historical-database in the current directory.
12. Have a coffee. This can take a while.
13. Run an interactive Docker container (i.e., one you can enter commands against) based on the image you just created with `docker run -it sandbox:bike-check-historical-database`
14. Check that the version of Python is what you expect (e.g., 3.11.6) by running `python`
15. Run `quit()` to leave the Python interpreter.
16. Exit all containers with `docker stop $(docker ps -a -q)`
