# Weatherapp

Hei!

I would like to say thank you for giving me the opportunity to attempt these tasks. I found them to be challenging, frustrating at times, and of course, rewarding. Through this README I will explain how to run the app both locally and with Docker, as well as how to install Docker and The Weather App using Ansible playbooks. 

As I had never used any of these technologies before, this whole process was a huge learning experience for me, so I will go into detail about what I did for each of the tasks, the challenges I faced as well as how I solved some issues (SEE WIKI).

## TO RUN THE APP WITH/WITHOUT DOCKER

### Clone this git repo using HTTPS

In order to run the app, you must first clone this repo, locally.
You can do this by following these simple steps:

1. Go to the repo (https://github.com/JordanClarkkk/weatherapp)

2. Click the 'Code' button

3. Copy the URL (https://github.com/JordanClarkkk/weatherapp.git)

4. Open your terminal and type 
```
git clone https://github.com/JordanClarkkk/weatherapp.git weatherapp
```
5. You can now open in your editor if you would like to view the files.

### To run the app with Docker, all you need to do is:

1. Open your terminal and type
```
docker volume create weatherapp
cd weatherapp
docker-compose -f docker-compose.yml -f docker-compose-with-reloading.yml up
```
2. Let the magic happen

3. Type 'localhost:8081' into the address bar of your browser

4. Now, you can dress appropriately for the Finnish 'spring'


### How to run the app locally without Docker

To run the app without Docker, all you need to do is:

1. Open your terminal and cd into the 'src' directory inside of the 'backend' directory.
2. Type:
```
npm i
npm run start
```
3. cd into the 'src' directory inside of the 'backend' directory and repeat:
```
npm i
npm run start
```
4. Open the app on localhost:8081!