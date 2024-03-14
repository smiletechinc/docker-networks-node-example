## 1 Node Assignment

### Command 1: Create docker image:
  ```
  $ docker build .
  ```
 Resultant Iamge Id: `8f1eb8d97a36`

### Command 1.1 Create docker image with custom name and tag
  ```
  $ docker build -t nodeappimage:v101
  ```

### Command 2: Run docker container
  ```
  $ docker run -p 8000:3000 8f1eb8d97a36
  ```
### Command 3: Stop docker container
  ```
  $ docker stop 8f1eb8d97a36
  ```

### Command 4: Recreate docker container with custom name
  ```
  $ docker run -p 8000:3000 --name nodeapp 8f1eb8d97a36
  ```

### Command 5: Delete stopped container
  ```
  $ docker rm nodeapp
  ```

### Command 5.1: Delete unused images
  ```
  $ docker rmi nodeappimage
  ```

### Command 6: Delete docker container when stopped
  ```
  $ docker run -p 8000:3000 -d --name nodeapp --rm 8f1eb8d97a36 
  ```
