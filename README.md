# Weatherapp

There was a beautiful idea of building an app that would show the upcoming weather. The developers wrote a nice backend and a frontend following the latest principles and - to be honest - bells and whistles. However, the developers did not remember to add any information about the infrastructure or even setup instructions in the source code.

## How to run the app locally with Docker
To run the app with Docker, all you need to do is:

1. Open your terminal and type
```
docker compose up
```
2. Let the magic happen

3. Type 'localhost:8081' into the address bar of your browser


## How to run the app locally without Docker

To run the app without Docker, all you need to do is:

1. Open your terminal and cd into the 'src' directory inside of the 'backend' directory.
Then type:
```
npm i
npm start
```
and then cd into the 'src' directory inside of the 'backend' directory and repeat:
```
npm i
npm start
```
Then, open the app on the port specified in the terminal!
