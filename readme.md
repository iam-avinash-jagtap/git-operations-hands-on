# Hands-on Git & Git Branching 
Hello, in this project, you will create a multi-page static website to understand and implement the concepts of Git and Git branching. The primary goal is to simulate a team-based development workflow using separate branches for each web page, reinforcing real-world version control practices. During the project, merge conflict errors were also resolved, providing hands-on experience in handling real Git scenarios.
## Learning Objectives
- Understand Git and branching.
- Create and manage branches.
- Simulate team development.
- Merge branches effectively.
- Build a multi-page website.
- Use VS Code for editing.
## Pre-requisites
- Basic knowledge of HTML and CSS.
- Conceptual understanding of Git.
- Git installed and configured on your system.
- Visual Studio Code (VS Code).
- A GitHub account.
- Familiarity with bash terminal.
- Web browser for testing pages.
# Step 1:- Initializing a Git repository for the project
_To initilize the git repository on your local machine you need to follow some steps._
1. Open your system.
2. Open project folder.
3. Right click - Open Git bash here
4. Follow commands - 

        git init 

       code .
##### Now you initalized a Git repository in the project directory and redirect on VS code 
# Step 2:- Create home page for the project
_Now you are in VScode, create home page of project in master/main branch._
1. Click on - New file 
2. Enter name - index.html
3. Enter HTML Script - 
```<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1">
  <title>Techaj - Home</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      background-color: #f4f6f8;
      text-align: center;
      padding: 50px;
    }
    h1 {
      color: #2c3e50;
    }
    .btn-container {
      margin-top: 40px;
    }
    .nav-btn {
      background-color: #3498db;
      color: white;
      border: none;
      padding: 15px 30px;
      margin: 10px;
      font-size: 18px;
      border-radius: 8px;
      cursor: pointer;
      transition: background-color 0.3s;
    }
    .nav-btn:hover {
      background-color: #2980b9;
    }
  </style>
</head>
<body>

  <h1>Welcome to Techaj 🌐</h1>
  <p>Select a category to explore:</p>

  <div class="btn-container">
    <button class="nav-btn" onclick="location.href='mobile.html'">📱 Mobile</button>
    <button class="nav-btn" onclick="location.href='laptop.html'">💻 Laptop</button>
    <button class="nav-btn" onclick="location.href='bike.html'">🏍️ Bike</button>
    <button class="nav-btn" onclick="location.href='car.html'">🚗 Car</button>
  </div>

</body>
</html>
```

4. Click on - Terminal 
5. Click on - New Terminal
6. Add new bash terminal 
7. Follow commands-

            git add index.html

            git status -s

            git commit -m "Added index.html file"

            git status -s 

![Home](https://github.com/iam-avinash-jagtap/git-operations-hands-on/blob/master/Images/Home.png)

#### You are created home page for your project in master branch
# Step 3:- Create Feature branches & pages respectively.
### Creating 1st feature branch - mobile 
_Now create mobile branch for add mobile.html page in your project._
1. Follow commands to create branch 

        git branch 

        git branch mobile 

        git checkout mobile 
2. Swtich on VS code editor
3. Enter HTML Script - 
```
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1">
  <title>Techaj - Mobile</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      background-color: #fffdf5;
      text-align: center;
      padding: 40px;
    }
    h1 {
      color: #2c3e50;
    }
    .brand-btn {
      background-color: #2ecc71;
      color: white;
      border: none;
      padding: 12px 25px;
      margin: 10px;
      font-size: 16px;
      border-radius: 6px;
      cursor: pointer;
      transition: background-color 0.3s;
    }
    .brand-btn:hover {
      background-color: #27ae60;
    }
  </style>
</head>
<body>

  <h1>📱 Mobile Brands</h1>
  <p>Select your favorite mobile brand:</p>

  <div>
    <button class="brand-btn">Apple</button>
    <button class="brand-btn">Samsung</button>
    <button class="brand-btn">OnePlus</button>
    <button class="brand-btn">Xiaomi</button>
    <button class="brand-btn">Realme</button>
    <button class="brand-btn">Vivo</button>
    <button class="brand-btn">Oppo</button>
    <button class="brand-btn">Motorola</button>
    <button class="brand-btn">Nothing</button>
    <button class="brand-btn">Infinix</button>
  </div>

</body>
</html>

```
4. Swtich to Terminal 

        git status -s

        git add .

        git commit -m "Added mobile.html file"

        git status -s

        git checkout master

        git merge mobile

![Mobile](https://github.com/iam-avinash-jagtap/git-operations-hands-on/blob/master/Images/Mobile.png)

#### Your Mobile page is ready using feature branch - Mobile
### Creating 2nd feature branch - laptop 
_Now create laptop branch for add laptop.html page in your project._
5. Follow commands to create branch 

        git branch 

        git branch laptop 

        git checkout laptop 
6. Swtich on VS code editor
7. Enter HTML Script - 
```
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1">
  <title>Techaj - Laptop</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      background-color: #f0f8ff;
      text-align: center;
      padding: 40px;
    }
    h1 {
      color: #34495e;
    }
    .brand-btn {
      background-color: #9b59b6;
      color: white;
      border: none;
      padding: 12px 25px;
      margin: 10px;
      font-size: 16px;
      border-radius: 6px;
      cursor: pointer;
      transition: background-color 0.3s;
    }
    .brand-btn:hover {
      background-color: #8e44ad;
    }
  </style>
</head>
<body>

  <h1>💻 Laptop Brands</h1>
  <p>Select your favorite laptop brand:</p>

  <div>
    <button class="brand-btn">Dell</button>
    <button class="brand-btn">HP</button>
    <button class="brand-btn">Lenovo</button>
    <button class="brand-btn">Asus</button>
    <button class="brand-btn">Acer</button>
    <button class="brand-btn">Apple</button>
    <button class="brand-btn">MSI</button>
    <button class="brand-btn">Samsung</button>
    <button class="brand-btn">Microsoft</button>
    <button class="brand-btn">LG</button>
  </div>

</body>
</html>
```
8. Swtich to Terminal 

        git status -s

        git add .

        git commit -m "Added laptop.html file"

        git status -s

        git checkout master

        git merge laptop

![Laptop](https://github.com/iam-avinash-jagtap/git-operations-hands-on/blob/master/Images/Laptop.png)

#### Your Laptop page is ready using feature branch - Laptop
### Creating 3rd feature branch - bike 
_Now create bike branch for add bike.html page in your project._
9. Follow commands to create branch 

        git branch 

        git branch bike 

        git checkout bike 
10. Swtich on VS code editor
11. Enter HTML Script - 
```
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1">
  <title>Techaj - Bike</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      background-color: #fff4f4;
      text-align: center;
      padding: 40px;
    }
    h1 {
      color: #c0392b;
    }
    .brand-btn {
      background-color: #e74c3c;
      color: white;
      border: none;
      padding: 12px 25px;
      margin: 10px;
      font-size: 16px;
      border-radius: 6px;
      cursor: pointer;
      transition: background-color 0.3s;
    }
    .brand-btn:hover {
      background-color: #c0392b;
    }
  </style>
</head>
<body>

  <h1>🏍️ Bike Brands</h1>
  <p>Select your favorite bike brand:</p>

  <div>
    <button class="brand-btn">Royal Enfield</button>
    <button class="brand-btn">Bajaj</button>
    <button class="brand-btn">Hero</button>
    <button class="brand-btn">Honda</button>
    <button class="brand-btn">TVS</button>
    <button class="brand-btn">Yamaha</button>
    <button class="brand-btn">Suzuki</button>
    <button class="brand-btn">KTM</button>
    <button class="brand-btn">BMW</button>
    <button class="brand-btn">Harley-Davidson</button>
  </div>

</body>
</html>
```
12. Swtich to Terminal 

        git status -s

        git add .

        git commit -m "Added bike.html file"

        git status -s

        git checkout master

        git merge laptop

![Bike](https://github.com/iam-avinash-jagtap/git-operations-hands-on/blob/master/Images/Bike.png)

#### Your Bike page is ready using feature branch - Bike
### Creating 4th feature branch - car 
_Now create car branch for add car.html page in your project._
13. Follow commands to create branch 

        git branch 

        git branch car 

        git checkout car 
14. Swtich on VS code editor
15. Enter HTML Script - 
```
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1">
  <title>Techaj - Car</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      background-color: #f3f9ff;
      text-align: center;
      padding: 40px;
    }
    h1 {
      color: #2d3436;
    }
    .brand-btn {
      background-color: #0984e3;
      color: white;
      border: none;
      padding: 12px 25px;
      margin: 10px;
      font-size: 16px;
      border-radius: 6px;
      cursor: pointer;
      transition: background-color 0.3s;
    }
    .brand-btn:hover {
      background-color: #0652dd;
    }
  </style>
</head>
<body>

  <h1>🚗 Car Brands</h1>
  <p>Select your favorite car brand:</p>

  <div>
    <button class="brand-btn">Tata</button>
    <button class="brand-btn">Hyundai</button>
    <button class="brand-btn">Maruti Suzuki</button>
    <button class="brand-btn">Mahindra</button>
    <button class="brand-btn">Honda</button>
    <button class="brand-btn">Toyota</button>
    <button class="brand-btn">Kia</button>
    <button class="brand-btn">BMW</button>
    <button class="brand-btn">Audi</button>
    <button class="brand-btn">Mercedes-Benz</button>
  </div>

</body>
</html>
```
16. Swtich to Terminal 

        git status -s

        git add .

        git commit -m "Added car.html file"

        git status -s

        git checkout master

        git merge car

![Car](https://github.com/iam-avinash-jagtap/git-operations-hands-on/blob/master/Images/Car.png)

#### Your Car page is ready using feature branch - Car
# Step 4:- Create and Resolve - Git code conflict.
_Now you are going to create and resolve Git code conflict issue._
### Creating 5th feature branch - about-us 
_Now create about-us branch for add about-us.html page in your project._
1. Follow commands to create branch 

        git branch 

        git branch about-us 

        git checkout about-us 
2. Swtich on VS code editor
3. Enter HTML Script - 
```
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1">
  <title>About Us - Techaj</title>
  <style>
    body {
      font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
      background-color: #fcfcfc;
      padding: 50px;
      line-height: 1.6;
      color: #2c3e50;
    }
    h1 {
      text-align: center;
      font-size: 36px;
      color: #2980b9;
    }
    .container {
      max-width: 800px;
      margin: auto;
      background-color: #ffffff;
      padding: 30px;
      border-radius: 10px;
      box-shadow: 0 0 15px rgba(0,0,0,0.1);
    }
    ul {
      list-style-type: "👉 ";
      padding-left: 20px;
    }
    li {
      margin: 12px 0;
    }
  </style>
</head>
<body>

  <div class="container">
    <h1>About Us - Techaj</h1>
    <p>Hello! Welcome to <strong>Techaj</strong> – your digital stop for exploring the best in Mobiles 📱, Laptops 💻, Bikes 🏍️, and Cars 🚗.</p>
    
    <p>Techaj is founded and developed by <strong>Avinash Jagtap</strong>, a passionate web developer and computer science enthusiast. Here's what makes Techaj unique:</p>

    <ul>
      <li>👨‍💻 Built by a full-time Computer Science student with a strong foundation in AWS, Azure & DevOps.</li>
      <li>🛠️ Designed as a practice project to implement real-world Git branching and team collaboration concepts.</li>
      <li>🌐 Organized by categories – Mobile, Laptop, Bike, and Car – with individual developers assigned to each section.</li>
      <li>🔧 Managed using version control with the Home Page acting as the central/main branch.</li>
      <li>🚀 Avinash aims to become a successful DevOps engineer, and Techaj reflects that journey in code.</li>
      <li>📈 Also runs an Instagram page with 4K+ followers sharing tech content.</li>
      <li>🏍️ Based in Pune, originally from Solapur, and loves bike rides & cricket!</li>
    </ul>

    <p>Stay tuned as we continue to grow and bring more tech info to your fingertips!</p>
  </div>

</body>
</html>
```
4. Edit index.html file
        _Add anchor tag for about-us.html file_
5. Swtich to Terminal 

        git status -s

        git add .

        git commit -m "Added about-us.html file & added anchor tag in index.html file"

        git status -s

        git checkout master

### Creating 6th feature branch - contact-us
_Now create contact-us branch for add contact-us.html page in your project._
6. Follow commands to create branch 

        git branch 

        git branch contact-us 

        git checkout contact-us 
7. Swtich on VS code editor
8. Enter HTML Script - 
```
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1">
  <title>Contact Us - Techaj</title>
  <style>
    body {
      font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
      background-color: #fdfefe;
      padding: 50px;
      color: #2c3e50;
    }
    .container {
      max-width: 700px;
      margin: auto;
      background-color: #ffffff;
      padding: 30px;
      border-radius: 12px;
      box-shadow: 0 0 15px rgba(0, 0, 0, 0.1);
    }
    h1 {
      text-align: center;
      color: #27ae60;
      margin-bottom: 30px;
    }
    label {
      display: block;
      margin: 15px 0 5px;
      font-weight: bold;
    }
    input, textarea {
      width: 100%;
      padding: 12px;
      border: 1px solid #ccc;
      border-radius: 6px;
      font-size: 16px;
    }
    textarea {
      resize: vertical;
      min-height: 100px;
    }
    button {
      background-color: #27ae60;
      color: white;
      padding: 12px 30px;
      border: none;
      border-radius: 6px;
      cursor: pointer;
      font-size: 16px;
      margin-top: 20px;
    }
    button:hover {
      background-color: #219150;
    }
  </style>
</head>
<body>

  <div class="container">
    <h1>📩 Contact Us</h1>
    <form>
      <label for="name">Your Name:</label>
      <input type="text" id="name" name="name" placeholder="Enter your name" required>

      <label for="email">Email Address:</label>
      <input type="email" id="email" name="email" placeholder="Enter your email" required>

      <label for="subject">Subject:</label>
      <input type="text" id="subject" name="subject" placeholder="Subject of your message" required>

      <label for="message">Your Message:</label>
      <textarea id="message" name="message" placeholder="Write your message here..." required></textarea>

      <button type="submit">Send Message</button>
    </form>
  </div>

</body>
</html>
```
9. Edit index.html file
        _Add anchor tag for contact.html file - Enter on same line of about-us.html_ 
10. Swtich to Terminal 

        git status -s

        git add .

        git commit -m "Added contact-us.html file & added anchor tag in index.html file"

        git status -s

        git checkout master

        git merge about-us 

        git merge contact-us
    _Warning.! -  code conflict error ouccers._
11. Resolve conflict error

            <<<<<<< HEAD
            // your changes
            =======
            // incoming branch changes
            >>>>>>> branch-name
    _Note:- Remove conflict text and resolve Conflict._

![About-us](https://github.com/iam-avinash-jagtap/git-operations-hands-on/blob/master/Images/About-us.png)

![Contact-us](https://github.com/iam-avinash-jagtap/git-operations-hands-on/blob/master/Images/Contact-us.png)

#### Your About Us and Contact Us pages are ready using their respective branches. 
# Step 5:- Delete Feature branches 
_When you are done with feature branch delete them.(Optional but recommended)_

        git branch -d mobile 

        git branch -d laptop

        git branch -d bike

        git branch -d car 

        git branch -d about-us

        git branch -d contact-us
# Summary 
This project shows an activity intended to exercise the Git and branching system through the practical task of building a multi-page static website. Each page was developed on separate branches to simulate team cooperation. The project emphasized regular commits and merging branches into the main version, along with resolving merge conflicts to offer real-world Git experience. HTML and basic CSS were used in VS Code to build the project while keeping the focus on version control.
Basically, this project served as an example of structured code management using Git, and also provided hands-on experience in resolving conflict errors during the merge process.