# Weatherapp

Through this README I will explain how to run the app both locally and with Docker, as well as how to install Docker and run the Weather App using Ansible playbooks. 

As I had never used any of these technologies before, this whole process was a huge learning experience for me, so I will go into detail about what I did for each of the tasks, the challenges I faced as well as how I solved some issues [(SEE WIKI)](https://github.com/JordanClarkkk/weatherapp/wiki/Eficode-WeatherApp-Tasks-Commentary).

## TO RUN THE APP WITH/WITHOUT DOCKER

### Clone this git repo using HTTPS

In order to run the app, you must first clone this repo, locally.
You can do this by following these simple steps:

1. Go to the repo (https://github.com/JordanClarkkk/weatherapp)

2. Click the 'Code' button

3. Copy the URL (https://github.com/JordanClarkkk/weatherapp.git)

4. Open your terminal and type 
```
git clone https://github.com/JordanClarkkk/weatherapp.git 
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

## TO USE ANSIBLE PLAYBOOKS TO INSTALL DOCKER AND RUN THE APP

##### Presuming you have already cloned the git repo and are in the appropriate directory, to use Ansible playbooks to automatically install Docker you should first:

1. Have ansible installed (https://docs.ansible.com/ansible/latest/installation_guide/intro_installation.html)

2. Find your IP address by typing:
```
ip a
```
into your terminal.

3. Configure Ansible hosts file: 
```
sudo nano /etc/ansible/hosts
```

4. Insert your machine:
```
[docker]
insert.ip.address.here
```

5. Add vars to hosts file:
```
[docker:vars]
ansible_user=type-username-here
ansible_password=password-here
ansible_become_passowrd=become-password-here
```
6. Now you can type
```
ansible-playbook ansible-install-docker.yml

```

7. Once the machine has done all of the work for you, to start Docker you simply type:
```
sudo service docker start
```

8. Now, you can check that Docker has started:
```
sudo service docker status
```

##### To run the weatherapp using Ansible playbooks:

1. Simply type:
```
ansible-playbook ansible-weatherapp.yml
```
into your terminal!

Now, the app should be available at localhost:8081
