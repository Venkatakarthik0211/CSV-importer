[![Review Assignment Due Date](https://classroom.github.com/assets/deadline-readme-button-24ddc0f5d75046c5622901739e7c5dd533143b0c8e959d652212380cedb1ea36.svg)](https://classroom.github.com/a/_IojtdoU)
# StackIt Hiring Assignment

### Welcome to StackIt's hiring assignment! 🚀

**If you didn't get here through github classroom, are you sure you're supposed to be here? 🤨**


We are glad to have you here, but before you read what you're going to beat your head over for the next few hours (maybe days?), let's get a few things straight:
- We really appreciate honesty. Don't copy anyone else's assignment, it'll only sabotage your chances :P
- You're free to use any stack, and library of your choice. Use whatever you can get your hands on, on the internet!
- We love out of the box solutions. We prefer to call it *Jugaad* 
- This might be just the first round, but carries the most importance of all. Give your best, and we hope you have a fun time solving this problem.

## ✨ **Problem Statement: Crafting a CSV Importer for Google Sheets** ✨

**Context**:
Data analysts around the world 🌍, handle massive amounts of data to derive meaningful insights for their organization 📊. Among the tools they use, Google Sheets 📈 stands out due to its ease of use, accessibility, and collaborative features. However, many analysts have identified a recurring pain point: the cumbersome process of importing CSV files into Google Sheets repeatedly.

A typical week of an analyst in an e-commerce company 🛒 involves receiving multiple CSV files 📁 containing sales, inventory, customer feedback, and more. The data from these files needs to be meticulously analyzed and presented in the company’s weekly meetings. However, instead of diving directly into analysis, most analysts need to spend an inordinate amount of time just importing and structuring these CSV files into Google Sheets ⏳. This repetitive, time-consuming task reduces the efficiency of these professionals and delays the extraction of crucial insights 😫.

**Today, you are going to make their lives better.**

**Problem Statement**:
Make a CSV Importer for Google Sheets that lets users drag and drop CSV files onto the Google Sheet. The moment they drop the CSV file, allow them to select which columns to import 🗂️.

You get brownie points 🍪 if you can make it even easier by allowing them to filter the data as well before importing it into Google Sheets 🔍.

**Other pointers**:
- Import to Sheet – After validation and mapping, devise a method to populate the data into a chosen Google Sheet, either appending to existing data or creating a new sheet 📥📋.
- Optimize for Large Files – Large datasets are common in analytics. Your solution should effectively handle large CSV files (~15MB CSV file) without causing performance issues or prolonged waiting times 📈📦.

## Submission ⏰
The timeline for this submission is: **9AM, 30th Sept, 2023 - 12PM, 2nd Oct, 2023**

Some things you might want to take care of:
- Make use of git and commit your steps!
- Use good coding practices.
- Write beautiful and readable code. Well-written code is nothing less than a work of art.
- Use semantic variable naming.
- Your code should be organized well in files and folders which is easy to figure out.
- If there is something happening in your code that is not very intuitive, add some comments.
- Add to this README at the bottom explaining your approach (brownie points 😋)

Make sure you finish the assignment a little earlier than this so you have time to make any final changes.

Once you're done, make sure you **record a video** showing your project working. The video should **NOT** be longer than 120 seconds. While you record the video, tell us about your biggest blocker, and how you overcame it! Don't be shy, talk us through, we'd love that.

We have a checklist at the bottom of this README file, which you should update as your progress with your assignment. It will help us evaluate your project.

- [✅] My code's working just fine! 🥳
- [✅] I have recorded a video showing it working and embedded it in the README ▶️
- [✅] I have tested all the normal working cases 😎
- [✅] I have even solved some edge cases (brownie points) 💪
- [✅] I added my very planned-out approach to the problem at the end of this README 📜

## Got Questions❓
Feel free to check the discussions tab, you might get something of help there. Check out that tab before reaching out to us. Also, did you know, the internet is a great place to explore 😛

## Developer's Section
*Add your video here, and your approach to the problem (optional). Leave some comments for us here if you want, we will be reading this :)*


Video link: https://drive.google.com/file/d/1l_Zzwx83wSz8qmXhS4NRLDZuUluaSj65/view?usp=drive_link

Planning : 📝

In the initial stages, I faced hurdles aligning the frontend and backend of the project. Harmonizing the user interface design (frontend) with the server logic and database (backend) proved to be a formidable challenge. 
Achieving seamless communication and data consistency demanded meticulous planning and coordination. 
However, through iterative testing and collaborative efforts, I ultimately achieved a harmonious integration of these two critical components.

Tech Stack:
- Front-end: HTML.CSS,JS 👩‍💻
- Back-end: Python(Flask, Dropzone), Google-sheets-api 🗄️ 

How i started to figure out solution? 🤔

- Backend Concentration: ✅
  I initially focused on the backend, learning Python Flask to build the server logic.

- Integration of File Upload: ✅
  I integrated Dropzone for drag and drop file uploads, ensuring a smooth user experience.

- Database Connection: ✅
  I established a connection to Google Sheets API to enable data storage and retrieval.

- JavaScript Customization: ✅
  I tackled the challenge of customizing JavaScript to fit my project's specific needs, such as handling API requests and user interactions.

- Frontend Development: ✅
  Lastly, I designed the frontend with a simple layout, ensuring a user-friendly interface that complements the backend functionality.

What's the challenging task i faced?
I faced hurdles aligning the frontend and backend of the project.

Process of Deployment: ⏳ 

Linux:  
 1. Install required packages
   ```sh 
   sudo apt-get update && sudo apt-get install python3-pip && pip3 install flask flask-dropzone gspread oauth2client pandas 
   ```
 2. Clone the Repository):
   ```sh 
   git clone https://github.com/StackItHQ/stackit-hiring-assignment-Venkatakarthik0211.git
   ```
 3. Run Flask Application(Deployment is ready in localhost)
   ```sh 
   python3 app.py
   ```
4. Navigate to Webpage, Upload <15MB file(If it 10-15MB, Select the desired column. It takes a minute to completely pre-process the data and export the csv to googlesheets if the size is greater than 10MB 🕒

Test cases: 

1. Only .csv files accepted ✅
2. <15MB only accepted ✅
3. If file is not uploaded, throws an alert ✅
4. Used pandas to export the csv files in form of dataframes and also to avoid appending the data in same column ✅
5. Duplicate columns which have same header names are ignored ✅
6. Brownie task is applied (Single .csv file) ✅

Future Work: 👨🏻‍💻

1. Automation became a daily part in our live. Dockerize and deploy the application in EKS, AKS or GKE for efficient use with public service accounts. 
   Ref: https://cloud.google.com/kubernetes-engine/docs/tutorials/authenticating-to-cloud-platform. 🐳

2. Pre-processing the daaa obtained is a huge obstacle, using cuda with jax in the backend, can increase performance. 🖥️
   Requirements: GPU-based computer

3. Performances related to frontend and API-based can be rectified using ML API's such as gradio-client 🔗

