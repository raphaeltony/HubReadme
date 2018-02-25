# Health Assistant Bot

This project was done as a part of the Hasura Product Development Internship. It is a custom service that integrates with wit.ai API and implements the features described below.

Entities used :

- Intent -  It extracts user intent from his query                

- Condition - It extracts the medical condition such as fever,cold,malaria etc. 

- Drug - It extracts the name of drug mentioned in user query such as aspirin, tetracycline etc.

When a query regarding an illness is asked, it will reply with its corresponding medicines. 
The frontend is built like a chat in which you one can converse with the 'assistant'.

# The Backend :

## How it works?

When the user sends a message, intent behind the text is extracted, analysed and the appropriate response is displayed. 

## The intents and its responses
1. findMedicine - It fetches drug for value of condition entity
2. findCondition - It fetches medical condition for value of drug entity
3. greeting
4. bye

## What does it use?
Hasura
Wit.ai API

## How do I use it in my workspace?
You can also clone and deploy from this link
https://hasura.io/hub/project/akshu/health-assistant

Install hasura CLI

1) Run the quickstart command
$ hasura quickstart akshu/health-assistant

2) Git add, commit & push to deploy to your cluster
$ cd health-assistant
$ git add . && git commit -m "First commit"
$ git push hasura master

Run hasura cluster status to find your cluster name.

It is all set. You can check the translation functionality in action in your workspace.

## How to build on top of this?
This service is written in javascript using nodejs-express framework. The source code lies in microservices/api/app/src directory. server.js is where you want to start modifying the code.

If you are using any extra packages, just add them to microservices/api/app/src/package.json and they will be 'npm installed' during the Docker build.

# The Frontend (App)

## Pre-requisites
- You will need Node, the React Native command line interface, Python2, a JDK, and Android Studio. If you haven't installed these, follow the steps in the "Build Projects with Native Code" tab of :
https://facebook.github.io/react-native/docs/getting-started.html

## Cloning the repository
- Assuming you have cloned the repository( Check above for instructions ), navigate into the react-native folder of the cloned repository
- Run the following command (Gitbash or some other linux-based terminal) :
```
npm install
```
- Install axios which will be used for making post requests
```
npm install axios
```
## Running the app on a device 
- Start your android emulator or connect your android phone via USB with USB Debugging enabled
- Run the following command from your project directory:
```
react-native run-android
```
- This will build and run the app on your emulator or device

## APK
Here's the link to the app APK : https://drive.google.com/file/d/19t66KBXK6pZ79W_zu1aYEFE0VdjSkIcZ/view?usp=sharing

## Using the app
- Type in your query and press the medkit button to send it to the bot.
- Examples of queries include :
```
Medicine for cold
What does aspirin cure ?
```

## How to build on top of this?
You can edit the files in src folder of the react-native app.

#### NOTE : We are constantly updating the database of illnesses and its corresponding medicines

# Support
If you find a bug, you can raise an issue here.

# Acknowledgements
- Akshatha S - * NodeJS Express *(Backend) - akshatha.s513@gmail.com 
- Raphael Tony - * React Native *(Frontend) - prince4raphael@gmail.com
- Rajeev Ranjan - * React JS *(Frontend) - talegarry1202@gmail.com
- Built on top of Hasura boilerplate hello-react

