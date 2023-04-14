# How to build Dockerfile and Docker Compose

Hello everyone,

Today I will show you how to build dockerfile and docker compose easily. Just read and apply!

## Install Docker (For Ubuntu)

- sudo apt-get update
- sudo apt-get install \ \
    ca-certificates \ \
    curl \ \
    gnupg

- sudo install -m 0755 -d /etc/apt/keyrings
- curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo gpg --dearmor -o /etc/apt/keyrings/docker.gpg
- sudo chmod a+r /etc/apt/keyrings/docker.gpg
- echo \
  "deb [arch="$(dpkg --print-architecture)" signed-by=/etc/apt/keyrings/docker.gpg] https://download.docker.com/linux/ubuntu \
  "$(. /etc/os-release && echo "$VERSION_CODENAME")" stable" | \
  sudo tee /etc/apt/sources.list.d/docker.list > /dev/null

- sudo apt-get install docker-ce docker-ce-cli containerd.io docker-buildx-plugin docker-compose-plugin

- sudo docker run hello-world (If this image will pull and print messages, Docker was downloaded successfully!

## Make Container

- Firstly, go into **Homework1** files and write **sudo docker build -t hello-internet** (by the way, you can change container name, example-name to what you want).
- Secondly, you can control your name of container with **sudo docker ps**.
- Thirdly, write **sudo docker run -d -p 80:80 CONTAINER_NAME** (also you can change ports). Docker container will start. You can observe localhost:80 on your browser.
- And finally, when you write **sudo docker stop CONTAINER_NAME**, docker container will stop.

## Run Docker Compose

- Firstly, you set name of your image in **docker-compose.yml**. You have to set what you did name last part of section. For example, I'll set **image: hello-internet**.
- After then, ,n **Homework1** file write **sudo docker compose up -d** your docker compose will work successfully and this working background through -d command.
- When you visit localhost:80, you'll see html page. And if you want to stop docker compose, you should write **sudo docker compose down** in your terminal.

Yepp, That's all! Now you know how to do it!
Congratulations!
