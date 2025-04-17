# 📚 MyLibraPy (CLI Version)

A simple command-line app for managing your personal library.  
This version is designed to be run as a Python script and is deployed on **Heroku as a worker dyno**.

---

## 📦 Features

- Add books to your collection  
- View and search your books  
- Edit and delete entries  
- Export to CSV  
- View statistics by genre and reading status  

---

## 🚀 Deployment

### ✅ Live Deployment (Heroku)

⚠️ **Note:** This is a CLI (Command Line Interface) app. It runs on Heroku as a background process (worker) and does **not** expose a web interface.

🔗 **Heroku app:**  
[https://mylibrapy-cli.herokuapp.com/](https://mylibrapy-cli.herokuapp.com/)  
👉 This will show an error if accessed via browser – that's expected for CLI apps.

---

## 📁 Repository

The source code for this deployment is available on GitHub:

🔗 [https://github.com/freewimoe/P3_MyLibraPy-Heroku](https://github.com/freewimoe/P3_MyLibraPy-Heroku)

You can also find:

- 🔹 The original CLI version:  
  [https://github.com/freewimoe/P3_MyLibraPy](https://github.com/freewimoe/P3_MyLibraPy)

- 🔹 An experimental Flask version (non-assessed):  
  [https://mylibrapy-flask-f0d2bbe3d176.herokuapp.com/](https://mylibrapy-flask-f0d2bbe3d176.herokuapp.com/)

---

## 🛠️ How Heroku Runs This CLI App

Heroku doesn't support interactive CLI apps (like `input()`) in a browser context.

This app is deployed using a `Procfile` that tells Heroku to launch:

```
worker: python my_libra.py
```

This launches the app as a **worker dyno**, which is suitable for background processes, not web frontends.

---

## 🧪 Local Testing

Since interactive CLI apps don't work via browser, you can run the app locally:

```bash
git clone https://github.com/freewimoe/P3_MyLibraPy-Heroku.git
cd P3_MyLibraPy-Heroku
pip install -r requirements.txt
python my_libra.py
```

---

## 📌 Notes for Reviewers

This project represents the **CLI version** of MyLibraPy and follows all requirements of the PP3 assignment brief.  
The Heroku deployment is included to demonstrate deployment skills, even though Heroku cannot accept live user input for CLI apps.  

All logic and features are fully functional and tested in a local environment.

---

## 👨‍💻 Author

**Friedrich-Wilhelm Möller**  
Code Institute Student – 2025 Cohort  
Germany 🇩🇪

![CI logo](https://codeinstitute.s3.amazonaws.com/fullstack/ci_logo_small.png)

Welcome,

This is the Code Institute student template for deploying your third portfolio project, the Python command-line project. The last update to this file was: **May 14, 2024**

## Reminders

- Your code must be placed in the `run.py` file
- Your dependencies must be placed in the `requirements.txt` file
- Do not edit any of the other files or your code may not deploy properly

## Creating the Heroku app

When you create the app, you will need to add two buildpacks from the _Settings_ tab. The ordering is as follows:

1. `heroku/python`
2. `heroku/nodejs`

You must then create a _Config Var_ called `PORT`. Set this to `8000`

If you have credentials, such as in the Love Sandwiches project, you must create another _Config Var_ called `CREDS` and paste the JSON into the value field.

Connect your GitHub repository and deploy as normal.

## Constraints

The deployment terminal is set to 80 columns by 24 rows. That means that each line of text needs to be 80 characters or less otherwise it will be wrapped onto a second line.

---

Happy coding!
