# Vue.js Mood Selector – Group Vue

## 1. Overview
This project is a **Vue.js tutorial application** created for the group vue
Tanishq • Mayank • Tamanna • Vaibhav

Our goal was to introduce Vue.js in a simple, fun, and interactive way using this simple mood selector app.

## BASIC FUNTIONING OF THE APP:
The user can:
- Pick a mood from a dropdown  
- See an emoji update instantly  
- Hear a sound effect based on the emotion choosne.
- Trigger a special mood (`?`)  (secret) 
- Watch the UI change automatically using Vue reactivity  
This project is intentionally small and easy to understand so the class can learn Vue.js quickly.

## 2. Learning Objectives of this demo:

After working with this demo, you guys will understand:
- How Vue.js works  
- How to use Vue via a CDN  
- How data is stored in `data()`  
- How reactive UI updates work  
- How to use:
  - `v-model`
  - `v-if`
  - `v-for`
  - `@click`
  - `@change`
- How functions inside Vue methods interact with HTML  
- How UI can change based on user selections

## 3. Tech Stack
Basic tech stack used for simplicity, nothing to be downloaded of installed seperately
- HTML – Structure  
- CSS – Comic-style UI  
- JS – Logic  
- VUE.JS CDN – Framework  
- GITHUB – Version control  

## 4. Project Structure
FOR THIS DEMO, TO KEEP IT SIMPLE, WE DID NOT CREATE A SEPERATE FILE FOR THE JS,
SIMPLY INTEGRATED IT INTO THE HTML
├── index.html # Main file (HTML + Vue script)
├── style.css # Page styling
├── sounds/ # Sound effects for moods
└── rick/ # GIF for the secret mood
└── r1.gif


## 5. How to Run the App
## Prerequisites
- Browser 
- VS Code (recommended)
- Live Server extension (recommended)

### Steps to make this work on your machine

1. Clone the repo:

```bash
git clone https://github.com/notax3l/VueEmojieDemo.git
cd VueEmojieDemo
```

2. Open the folder in VS Code

3. Start the app:
Option A — Live Server
Right-click → Open with Live Server
Option B — Manual
Double-click index.html

6. How the Mood Selector Works
--User selects a mood
v-model="selectedMood" stores it in Vue
--Vue updates:
Emoji
Message
Background color
--Vue plays a sound using playSound()
--Clicking emoji replays the sound
--Secret mood (?) displays a fullscreen GIF
--This shows how Vue automatically updates the UI when data changes.

                            ##IN CLASS EXERCISE FOR VUE##

We are going to be creating a Vue app that changes text when a button is clicked.

STEPS:
1.Create a new file: exercise.html
2.Add HTML + Vue CDN:
(copy and paste this code in your index)

<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>Vue Exercise</title>
  <script src="https://unpkg.com/vue@3/dist/vue.global.js"></script>
</head>
<body>

  <div id="app">
    <h2>{{ message }}</h2>
    <button @click="changeMessage">Click Me</button>
  </div>

  <script>
    const app = Vue.createApp({
      data() {
        return {
          message: "Welcome to Vue!"
        };
      },
      methods: {
        changeMessage() {
          this.message = "Hello from Vue.js!";
        }
      }
    });

    app.mount("#app");
  </script>

</body>
</html>

3.RUN IT IN A LIVE SERVER.

##Important Vue Code Used##
CODE:
const app = Vue.createApp({
  data() {
    return {
      selectedMood: "",
      currentAudio: null,
      moods: [ /* mood objects */ ]
    };
  },
  methods: { playSound(), emojiClicked() }
});

app.mount("#app");

DETAILS:
--data() contains the app state

--methods contains functions for sounds

--Vue attaches to <div id="app">

CODE:
<select v-model="selectedMood" @change="playSound">
  <option v-for="mood in moods" :value="mood">
    {{ mood.label }}
  </option>
</select>

DETAILS:
--v-model = dropdown selection stored in Vue

--v-for = loop through moods[]

--@change = play sound

LINKS TO THE DEMO:

WEATHER VIEW APP DEPLOYMENT:
https://stately-sundae-436f4c.netlify.app/

LINK TO THE PROJECT REPO:
https://github.com/Mayank-p-22/Group-project-

BY-
TANISHQ PRATAP SINGH
MAYANK PAL
VAIBHAV NARULA
TAMANNA TAMANNA
