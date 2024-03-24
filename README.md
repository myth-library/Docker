# Linux for Docker

## Workflow

- Pull ubuntu image from docker hub

  ```
  docker pull ubuntu
  ```

  ```sh
  docker run ubuntu  # automatically pull if the image not exists
  ```

- Run ubuntu image in a interactive mode

  ```sh
  docker run -it ubuntu
  ```

- Basic shell commands

  ```sh
  echo hello

  whoami

  echo $0

  history
    !2
  ```

<br />

- Managing packages

  - ubuntu package manager = apt (advanced package tool)

  ```sh
    apt
    apt-get

    apt update  # update package database

    apt install nano
    apt remove nano
  ```

<br />

- Navigating file system

  ```sh
  pwd

  ls -1
  ls -l

  cd ~  # use go to home directory of currently logged in user

  ```

  ```sh
  mkdir test
  mv test docker  # rename or move files/folders
  touch hello.txt  # to create new file
  mv hello.py test.txt
  touch file1.txt file2.txt ...

  rm file1.txt file2.txt
  rm file*
  rm -r docker/  # to remove folder
  ```

  - ctrl + w --> remove entire word in one go
