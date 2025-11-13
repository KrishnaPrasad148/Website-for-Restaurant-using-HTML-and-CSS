# EX07 Creating a Restaurant Website using HTML and CSS

### Date: 13/11/25  

---

## AIM:
To create a restaurant website using HTML and CSS that displays the restaurant’s menu, booking options, and other details in a well-structured and visually appealing layout.


## DESIGN STEPS:

### Step 1:
Create a new folder.

### Step 2:
Inside the folder, create the following files:
- `index.html`
- `styles.css`

### Step 3:
Design the website layout using HTML including the header, navigation bar, hero section, main content, and footer.

### Step 4:
Use CSS to style the elements with colors, typography, and layout (flexbox for alignment).

### Step 5:
Test the website in a browser and make sure it adapts well to different screen sizes.

### Step 6:
Add hover effects, background images, and shadow effects to improve interactivity.

### Step 7:
Review and finalize the design.



## PROGRAM:
```
Developed By : Krishna Prasad S  
Register No. : 212223230108 

```


### index.html
```html

<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>MEET n EAT</title>
  <link rel="stylesheet" href="styles.css">
</head>
<body>

  <!-- Header Section -->
  <header class="header">
    <div class="logo">
      <img src="logo.png" alt="MEET n EAT">
    </div>
    <nav class="nav-bar">
      <ul>
        <li><a href="#">HOME</a></li>
        <li><a href="#">MENU</a></li>
        <li><a href="#">BOOK</a></li>
        <li><a href="#">ABOUT</a></li>
      </ul>
    </nav>
  </header>

  <!-- Hero Section -->
  <section class="hero">
    <div class="hero-content">
      <h2>Juicy Bites, Happy Nights!</h2>
      <p>Welcome to <b>Grill & Chill Burgers</b> — where every bite is packed with smoky flavor, crispy fries, and smiles all around. Come hungry, leave happy!</p>
    </div>
  </section>

  <!-- Main Content -->
  <main class="main-content">
    <section class="card">
      <h3>Our New Menu</h3>
      <img src="menu.jpg" alt="New Menu">
      <p>From classic cheeseburgers to spicy BBQ delights. Explore our menu full of juicy, handcrafted burgers made with love.</p>
      <a href="#">See our new menu</a>
    </section>

    <section class="card">
      <h3>Book a table</h3>
      <img src="table2.jpg" alt="Book a Table">
      <p>Want the best seat in the house? Reserve your table now and enjoy the perfect meal in a cozy, burger-filled vibe.</p>
      <a href="#">Book your table now</a>
    </section>

    <section class="card">
      <h3>Opening Hours</h3>
      <img src="chef.jpg" alt="Opening Hours">
      <ul>
        <li> Mon - Fri: 2pm - 10pm</li>
        <li> Sat: 2pm - 11pm</li>
        <li> Sun: 2pm - 9pm</li>
      </ul>
    </section>
  </main>

  <!-- Footer -->
  <footer class="footer">
    <img src="logo1.png" alt="MEET n EAT" class="footer-logo">
    <p>Copyright MEETnEAT*</p>
  </footer>

</body>
</html>

```
### styles.css
```css
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
  font-family: 'Verdana', sans-serif;
}

body {
  background-color: #000000;
}

/* Header Section */
.header {
  background-color: #000000;
  text-align: center;
  padding: 20px;
}

.logo {
  display: flex;
  flex-direction: column;
  align-items: center;
}

.logo img {
  width: 300px;
  height: 200px;
}

.logo h1 {
  font-size: 28px;
  color: #ffffff;
  letter-spacing: 2px;
  text-transform: uppercase;
}

/* Navigation */
.nav-bar {
  background-color: #434343;
  margin-top: 20px;
  border-radius: 20px; 
}

.nav-bar ul {
  display: flex;
  justify-content: flex-start; 
  list-style: none;
  padding: 10px 40px;
}

.nav-bar li {
  margin: 0 20px;
}

.nav-bar a {
  color: white;
  text-decoration: none;
  font-weight: bold;
  position: relative;
  transition: color 0.3s ease;
}

.nav-bar a::after {
  content: '';
  position: absolute;
  left: 0;
  bottom: -5px;
  width: 0%;
  height: 2px;
  background-color: #ffcc33;
  transition: width 0.3s ease;
}

.nav-bar a:hover {
  color: #ffcc33;
}

.nav-bar a:hover::after {
  width: 100%;
}

/* Hero Section */
.hero {
  position: relative;
  border-radius: 20px;
  color: rgb(255, 255, 255);
  text-align: left;
  padding: 60px 40px;
  margin: 20px auto;
  width: 90%;
  overflow: hidden;
}

.hero::before {
  content: "";
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background: url('burger.png') center/cover no-repeat;
  filter: blur(6px);
  z-index: 0;
}

.hero-content {
  position: relative;
  z-index: 1;
  background: rgba(0, 0, 0, 0.4);
  backdrop-filter: blur(5px);
  padding: 30px;
  border-radius: 15px;
  transition: transform 0.3s ease, box-shadow 0.3s ease;
}

.hero-content:hover{
  transform: translateY(-2px) scale(1.01);
  box-shadow: 0 4px 8px rgba(0, 0, 0, 0.6);
}

.hero-content h2 {
  font-size: 32px;
  font-weight: bold;
  text-shadow: 2px 2px 4px #000;
}

.hero-content p {
  max-width: 600px;
  margin-top: 10px;
}

/* Main Content */
.main-content {
  display: flex;
  justify-content: center;
  gap: 20px;
  margin: 20px auto;
  width: 90%;
}

.card {
  background-color: #FAEBD7;
  padding: 15px;
  border-radius: 20px;
  flex: 1;
  text-align: left;
  box-shadow: 0 4px 8px rgba(0, 0, 0, 0.2);
  transition: transform 0.3s ease, box-shadow 0.3s ease;
}

.card:hover {
  transform: translateY(-2px) scale(1.01);
  box-shadow: 0 4px 8px rgba(255, 204, 51, 0.6);
}

.card h3 {
  margin-bottom: 10px;
  color: #333;
}

.card img {
  width: 100%;
  border-radius: 10px;
  margin-bottom: 10px;
}

.card p {
  color: #333;
  margin-bottom: 10px;
}

.card a {
  display: inline-block;
  color: #464b7c;
  text-decoration: none;
  font-weight: bold;
  padding: 10px 15px;
  border: 2px solid rgba(32, 34, 47, 0.6); 
  border-radius: 8px;
  background-color: rgba(255, 255, 255, 0.1); 
  transition: all 0.3s ease;
}

.card a:hover {
  background-color: rgba(255, 255, 255, 0.1); 
  border-color: #2d82ea; 
  color: #3399ff;
  transform: scale(1); 
}

/* Footer*/
.footer {
  display: flex;
  justify-content: space-between;
  align-items: center;
  background-color: #000000;
  padding: 20px 50px;
  margin-top: 30px;
  border-radius: 15px;
}

.footer-logo {
  width: 50px;
}

.footer p {
  color: #FAEBD7;
}

```


## OUTPUT:
<img width="1919" height="920" alt="web1" src="https://github.com/user-attachments/assets/5785eb82-e99a-4b16-97a1-b19d014d7bd6" />

<img width="1895" height="910" alt="web2" src="https://github.com/user-attachments/assets/06bad8ba-3059-4317-b1a0-019c8262d27e" />

<img width="1919" height="923" alt="web3" src="https://github.com/user-attachments/assets/0108921b-1d72-4b4c-8309-99acb7bf05e4" />

## RESULT:
The Restaurant Website was successfully created using **HTML and CSS** with a clean and responsive design.
