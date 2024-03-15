## Steps to run this docker container

### Step 1: Create a docker image
  ```
  $ docker build -t docker-image .
  ```

### Step 2: Create netowork
  ```
  $ docker network create docker-network
  ```

### Step 3: Start mongo db contaier in network
  ```
  $ docker run -d --name mongodb --network docker-network mongo
  ```

### Step 4: Start docker container
  ```
  $ docker run -p 3000:3000 --name docker-container --rm docker-image
  ```

### Step 5: Show logs
  ```
  $ docker logs docker-container
  ```
