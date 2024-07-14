# A2SV-hackthon
### Project Ideas
- Nested: 
#### Inspiration
27 million people move to cities every year in the US, and moving is listed as one of the top 5 most stressful life events according to verywellmind.com.

Each of our team members has moved in the past year, and we all felt overwhelmed as we not only had to move our stuff, but also move our habits and routines. We had to answer the questions: where should I buy groceries, where will I get my haircut, what doctor should we see, and more? And it would take a few months to find these answers, often requiring asking friends for advice, and spending hours on forums and navigation tools.

We wondered, is there a more efficient way to discover the nest of places that will make up our lives in a new city?

#### What it does
So we built Nested. Nested helps you move to a new city with ease by matching you with places based on your lifestyle. It analyzes your google maps search history to understand your preferences, and then provides tailored suggestions to nearby grocery stories, gyms, museums, or any type of place you can think of!

#### Technologies to be Used
Frontend: React, TypeScript, Material UI
Backend: Flask, Python
APIs: Google Places API, Distance Matrix API, Geocoding API, Identity Toolkit API, Maps Javascript API, Generative Language API, Token Service API, Google Drive API, & People API
Database and Authentication: Firebase

### Project link
- [Nested](https://devpost.com/software/nested)

## Ever English
#### Inspiration
For this project, I wanted to take advantage of the core functionality of Gemini AI: processing language and generating text. With Gemini's advanced reasoning, I took the idea of language processing to the next level: teaching language, specifically the English language.

I used Gemini in Google's AI studio to simulate English conversations, and it seemed to do that very well. Then I used it to ask me English proficiency test exercises -- it did that very well, too. THEN I asked it to tailor these exercise questions to a certain proficiency level, which I found it could also accurately do. Finally, I asked it to generate these exercises in a consistent JSON format. So far, I haven't found any problems.

With these in mind, I moved forward to creating Ever English, to create a web app able to generate unique and dynamic English exercises on the go using Google's Gemini AI.

I aimed to allow users to be given exercises befitting their proficiency. I would also track their progress, and, thanks to AI, adapt the generated exercise to match their increasing proficiency.

#### What it does
Ever English is an online English learning platform. Users start from zero and level up their proficiency through participating in fun English exercises and quizzes to gain enough experience to get to each next level. These exercises are dynamic because they are generated through Gemini and takes into account the user level and appropriate concepts that someone at a particular level should learn.

There are currently 4 types of exercises users can do (I will provide a quick link to try each exercise type, but you have to be logged in first):

#### Technologies to be used
- Gemini AI
The core of this application. Gemini was used to query for JSON objects representing the different kinds of exercise based on appropriate concepts and the user's level. This JSON is then used to render the quizzes the user will view.

- Appwrite
Appwrite provides seamless authentication as well as needed data storage and event responses. For example, upon user registration, Appwrite functions will generate a corresponding userLevel row in the database to store each user's level to track their progress.

- NextJs
NextJs sticks the whole thing together to make one app. It's used as the frontend. The app router's route handlers were used to call upon Gemini to generate exercises without exposing API keys.