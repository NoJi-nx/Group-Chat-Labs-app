[![Review Assignment Due Date](https://classroom.github.com/assets/deadline-readme-button-24ddc0f5d75046c5622901739e7c5dd533143b0c8e959d652212380cedb1ea36.svg)](https://classroom.github.com/a/CViV37hj)

# u08 -Business Idea

<span style="color:#; font-family: ; font-size: 4em;">Chat</span> <span style="color:#8B5CF6;font-family: ; font-size: 4em;">Labs</span>

![Chat Labs logo](/chatlabs/src/assets/logo2.png "Chat Labs logo")

# Innehållsförteckning

1. [Installation](#installation)
2. [Kodbas](#kodbas)
3. [Användning](#användning)
4. [Dokumentation](#dokumentation)
5. [Bidragarna](#bidragarna)
6. [Licens](#licens)

# Installation

To get started with this project, follow the steps below:

Clone the repository to your computer:
git clone https://github.com/zamero/u08-business-idea-grupp3-u08
<br>Navigate to the project directory:
Bash
cd chatlabs

Install frontend dependencies with npm:

npm install

Install backend dependencies with npm:
cd ../backend
npm install
Set up MongoDB databas:
Go to app.js in the backend
and change the const dbURI = {your MongoDB URI}

Get it working in localhost:
Change all the instances of "https://chatlabs.up.railway.app/" to http//:localhost:4000/
in the frontend. and create an .env in the frontend with google Oauth key

VITE_CLIENT_ID=googleOAUTHAPI

and in the backend you need another .env file that has the following api keys:
NODE_ENV=development
PORT= 4000
OPENAI_API_KEY=sk-XXX
ELEVENLABS_KEY=5facXXX

Once you got that solved you can use 2 bash consoles to npm run dev in both the backend file and the chatlabs(frontend file)

# Kodbas

Projektet består av följande kodbaser/komponenter

### 1. **Frontend**:

* Description: The frontend codebase is responsible for the user interface and client-side functionality.
* Technologies/Libraries Used: React, HTML, CSS (Tailwind), JavaScript, etc.
* Directory Structure:
    * chatlabs/: main map for frontend
        * .env:
        * src/: contains source code
             * components/: 
                 * CharacterForm.tsx:
                 * ChatPrompt.tsx:
                 * Footer.tsx:
                 * NavBar.tsx:
                 * Steps.tsx: .
            <br>
             * pages/: 
                 * Dashboard.tsx:
                 * db-2.tsx:
                 * db-4.tsx:
                 * FormModal.tsx:
            * App.tsx:
            * index.css:
            * main.tsx :

              
             

### 2. **Backend**:

* Beskrivning: Handles server-side logic and interacts with databases or external APIs.
* Technologies/Libraries Used: Node.js, Express, MongoDB/Mongoose, etc.
* Directory Structure:
    *  backend/: main map for backend. 
        * **'.env'**: contains environment variables used in the application:
            * **'NODE_ENV'**: Specifies the environment mode, usually set to development in this case.
            * **'PORT'**: Specifies the port on which the server will listen for incoming requests, set to 4000.
            * **'OPENAI_API_KEY'**: API key for OpenAI GPT-3.5 Turbo model, used for generating responses.
            * **'ELEVENLABS_KEY'**: API key for Eleven Labs text-to-speech API, used for converting text to audio.

        * **'app.js'**: the entry point of the application and sets up the Express server:

            * Importing necessary packages such as express, cors, fs, mongoose, axios, and body-parser.

            *  Using dotenv package to load environment variables from the **.env** file.

            * Configuring middleware for request handling, including cors to enable cross-origin resource sharing, and body-parser to parse JSON and URL-encoded data.

            * Establishing a connection to the MongoDB database using the mongoose package.

            * Routes setup: Defining various routes using app.put(), app.delete(), app.post(), and app.get() methods. These routes handle different CRUD operations for the user characters.

            
        * **'userCRUD.js'**: Exports functions for performing CRUD operations on user characters:

             * **'create'**: Creates a new user character by saving it to the database.
            * **'readAll'**: Retrieves all user characters from the database.
            * **'read'**: Retrieves a specific user character based on the provided id.

        * **userSchema.js**: Defines the Mongoose schema for the user and character objects:
            * **'email'**: String field representing the email of the user. It is required.
            * **'sub'**: String field representing a subject, not required.
            * **'Characters'**: An array field containing objects representing user characters. Each character object has the following properties:

            * **'name'**: String field representing the name of the character. It is required.
            * **'backstory'**: String field representing the backstory of the character. It is required.
            * **'traits'**: String field representing the traits of the character. It is required.

# Användning

## Chat labs is a Chat NPC service for game developers to make AI generated interactive NPC:s for their games.

### Example use case:

You are creating a game set in a world where magicians and humans live along side each other. A dragon is said to threaten the village, and living somewhere in the mountains. You need a character guiding your main character to the mountains and provide them with information. Create that character with Chat labs! Just write a short backstory, give the NPC a name and personality traits, hit _create_ and there you have it! You can now chat with the character, saying what you want them to say and download the sound file to use in your game.

This is not limited to video games, but can also be used in a more traditional board game context, for example D&D. Just have fun and be creative!

Happy developing!
/ Chat labs team

# Dokumentation

Daily-Scrums:
https://docs.google.com/document/d/1LMuhqvmej-LUDXtamVxOSvMyaCqgHevOQF9dOItwGDQ

Mongoose Schema:
https://cdn.discordapp.com/attachments/1103323453068673124/1105118330131599380/ER-diagram-v2.png

Figma initial sketch:
https://www.figma.com/file/r8tbrfqE1j1VS8NlltcdzL/The-AI-Artist?type=design&node-id=0-1&t=Xlo4QOVlnC3OZNYj-0

# Bidragarna

Samer Essam
https://github.com/zamero
https://www.linkedin.com/in/samer-essam-9908b41a2/

Ghanemla lamloumi
https://github.com/Ghanemla

Isabelle Johannesson
https://github.com/isabellejohannesson
https://www.linkedin.com/in/isabellejohannesson

Sandra Rehnström
https://www.linkedin.com/in/sandra-rehnstr%C3%B6m-54a547188/

Nejirwan Ramadan
https://github.com/NRiCe31
https://www.linkedin.com/in/nejirwan-ramadan/

Camilla Gustafsson
https://github.com/Camgus89
https://www.linkedin.com/in/camilla-gustafsson-1951aa136/

# Licens

MIT LICENSE:
https://github.com/zamero/u08-business-idea-grupp3-u08/blob/main/LICENSE
