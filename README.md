# gauntlt-docker
The docker for gauntlt

## How it works
This is not a traditional docker container. It is purposely made to get started with security testing with gauntlt. There are a couple things we do here that are a bit different.

- Arachni and nikto are installed inside this container
- Gauntlt is installed and is set as the entrypoint
- You can run `make install-stub` and on your host machine you will be able to just run `$ gauntlt-docker` as if you were running `$ gauntlt` in your host. It's neat but not conventional.

Feel free to fork this and customize for your needs. This container is great to put into a CI/CD pipeline and many people use it for this purpose.

## Setup

1. Clone this repo
  ```
  git clone https://github.com/samboleap/DevSecOps-gauntlt-docker.git
  ```

2. Build the docker container

  ```
  $ cd /path/to/cloned/repo/gauntlt-docker
  $ make build
  ```

3. Check out what `make` can do for you
  ```
  $ make help
  ```

4. Copy binary stub to your $PATH (like `/usr/local/bin`)
  ```
  $ make install-stub
  ```

5. Test it out with a `gauntlt-docker --help`

6. You can get interactive access to the container to test attack tools installed
  ```
  $ make interactive
  ```
