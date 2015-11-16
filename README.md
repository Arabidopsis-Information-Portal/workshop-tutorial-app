# AIP Developer Workshop

## Creating AIP Science App using Yeoman Generator

## 1. Installing Yeoman Generator
Run the next command in the terminal.
```
$ npm install aip-science-app
```

## 2. Create folder.
Run the next command to create the folder where your Science App will live locally.
```
$ mkdir <scienca-app-name>
```

We'll be using `my-new-science-app` for the rest of this tutorial.

## 3. Run Yoman Generator
```
$ yo aip-science-app
```

After running the previous command you'll have to answer a few questions:
- How would you like to name your science app? 
  - **Type:** string
  - **Notes:** This will be the title that appears on the portal.
  - **Required:** True
- What's the name space for this science app?
  - **Type:** string
  - **Validation:** only alphanumeric characters and `-`, ` _ `.
  - **Notes:** Use this if the science app will be build against a specific ADAMA service. This is the name space of such ADAMA service. It will help the generator to create an example of a call to an ADAMA service. Used together with a service (next question).
  - **Rquired:** False
- Which service are you going to use?
  - **Type:** string
  - **Validation:** only alphanumeric characters and `-`, ` _ `.
  - **Notes:** Use this if the sicence app will be build against a specific ADAMA service. This is the name of the service.
  - **Rquired:** False
- Give a quick description of this science app.
  - **Type:** text
  - **Notes:** This description will be used in the app manifest and displayed in the science app template.
  - **Required:** False
- How would you like to name the main HTML file?
  - **Type:** string
  - **Validation:** only alphanumeric characters and `-`, ` _ `:
  - **Default:** main.html
  - **Required:** False
- What about the main js file? (You can add more later).
  - **Type:** string
  - **Validation:** only alphanumeric characters and `-`, ` _ `:
  - **Default:** main.js
  - **Notes:** Every custom javscript file created for the app must be added into the `scripts` array in the app's manifest.
  - **Required:** False
- And the main css file? (You can add more later).
  - **Type:** string
  - **Validation:** only alphanumeric characters and `-`, ` _ `:
  - **Default:** main.css
  - **Notes:** Every custom css file created for the app must be added into the `styles` array in the app's manifest.
  - **Required:** False
- Where do you want to keep your stylesheets?.
  - **Type:** string
  - **Validation:** only alphanumeric characters and `-`, ` _ `:
  - **Default:** styles
  - **Notes:** Folder name to use when creating folder to hold styles files. This folder will be created under your `app` folder structure.
  - **Required:** False
- Where do you want to keep your scripts?
  - **Type:** string
  - **Validation:** only alphanumeric characters and `-`, ` _ `:
  - **Default:** scripts
  - **Notes:** Folder name to use when creating folder to hold scripts files. This folder will be created under your `app` folder structure.
  - **Required:** False
- Would you like to use any of the following libraries?
  - **Type:** radio button
  - **Default:** None
  - **Notes:** Use this if you want to add any of the listed libraries automatically.
  - **Required:** False

## 4. Install dependencies.
Run the following command
```
$ npm install
```
This will install any dependencies necessary.
## 5. Run basic app.
Run the following command
```
$ grunt
```
The basic app will run in your browser.

## 6. Fill in the authentication form.
When the basic application is first run you will need to fill in your username, password, consumer key and secret key. This so the library can ask for an OAuth Agave token.

## 7. Inspect basic application.
Once the basic application has a key to comunicate to Agave, it will display a summary of the different functions one can use with the library.

If the correct **namespace** and **service name** was given, it will also display a table with the first 10 records of the */list* endpoint. This is as an example of what you can do with a science application. 

We will talk more about this in the next steps.
