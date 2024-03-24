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

<br />

- Edit & view files

  ```sh
  nano docker.txt
    # ctrl + x --> Y --> confirm file name + enter

  cat docker.txt

  more docker.txt  # only for scroll down
      # press `enter` to read line by line
      # press `space` to go to next page
      # press `q` to exit

  apt install less
  less docker.txt
      # up & down arrows to scroll up & down
      # press `enter` to read line by line
      # press `space` to go to next page
      # press `q` to exit

  head -n 5 docker.txt
      # first 5 line displayed

  tail -n 5 docker.txt
      # last 5 line displayed
  ```
