# Ex02 - Commercial Website
## Date:13.08.2025

## AIM
To create a commercial website using CSS Flexbox.

## ALGORITHM
### STEP 1
Create an HTML file (index.html)

### STEP 2
Create a CSS file (style.css)

### STEP 3
Include a navigation bar with links to different sections.

### STEP 4
Add structured sections for Homepage, Products / Services, About Us, Contact Details and User Account.

### STEP 5
Include social media links at the footer with copyright information.

### STEP 6
Define global styles for fonts, colors, and layout.

### STEP 7
Style the header, navigation bar, and sections.

### STEP 8
Use Flexbox for layout design.

### STEP 9
Add hover effects and transitions for interactivity.

### STEP 10
Add Images and Media.

### STEP 11
Use optimized images for a professional look.

### STEP 12
Open the HTML file in a browser to check layout and functionality.

### STEP 13
Fix styling issues and refine content placement.

### STEP 14
Deploy the website.

### STEP 15
Upload to GitHub Pages for free hosting.

## PROGRAM
```
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>GOODLIFE</title>
  <link rel="stylesheet" href="style.css">
  <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0/css/all.min.css">
</head> 
<body>
    <style>
body {
  font-family: Verdana, Geneva, Tahoma, sans-serif;
  margin: 0;
  padding: 0;
  line-height: 1.6;
  background: linear-gradient(135deg, #e3f2fd, #ffffff);
  color: #222222;
}

.container {
  max-width: 1200px;
  margin: 0 auto;
  padding: 0 20px;
}

/* Buttons */
.btn {
  display: inline-block;
  background-color: #0288d1;
  color: #ffffff;
  padding: 12px 25px;
  text-decoration: none;
  border-radius: 5px;
  transition: background-color 0.3s ease, box-shadow 0.3s ease;
  box-shadow: 0 2px 5px rgba(2, 136, 209, 0.3);
}
.btn:hover {
  background-color: #ff7043;
  box-shadow: 0 4px 10px rgba(255, 112, 67, 0.5);
}

/* Navbar */
.navbar {
  background-color: #ffffff;
  padding: 15px 0;
  position: sticky;
  top: 0;
  z-index: 1000;
  box-shadow: 0 2px 8px rgba(0,0,0,0.1);
}
.navbar .container {
  display: flex;
  justify-content: space-between;
  align-items: center;
}
.navbar .logo {
  font-size: 1.8em;
  font-weight: bold;
  color: #0288d1;
  text-decoration: none;
}
.navbar .nav-links {
  list-style: none;
  display: flex;
}
.navbar .nav-links li {
  margin-left: 25px;
}
.navbar .nav-links li a {
  color: #333333;
  text-decoration: none;
  transition: color 0.3s ease;
}
.navbar .nav-links li a:hover {
  color: #0288d1;
}

/* Hero */
.hero {
  background-image: linear-gradient(rgba(2, 136, 209, 0.6), rgba(2, 136, 209, 0.6)), url('hero-bg.jpg');
  background-size: cover;
  background-position: center;
  color: #ffffff;
  text-align: center;
  padding: 150px 0;
}
.hero h1 {
  font-size: 3em;
  margin-bottom: 20px;
  text-shadow: 2px 2px 5px rgba(0,0,0,0.5);
}
.hero p {
  font-size: 1.2em;
  margin-bottom: 30px;
  text-shadow: 1px 1px 3px rgba(0,0,0,0.4);
}

/* Products */
.products {
  padding: 80px 0;
}
.products h2 {
  text-align: center;
  margin-bottom: 50px;
  color: #0288d1;
}
.product-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
  grid-gap: 30px;
}
.product {
  background-color: #ffffff;
  border-radius: 8px;
  box-shadow: 0 4px 10px rgba(0,0,0,0.1);
  overflow: hidden;
  transition: transform 0.3s ease, box-shadow 0.3s ease;
}
.product:hover {
  transform: translateY(-5px);
  box-shadow: 0 6px 15px rgba(2, 136, 209, 0.3);
}
.product img {
  width: 100%;
  height: auto;
  display: block;
}
.product h3 {
  color: #333333;
  margin: 20px 0 10px;
  text-align: center;
}
.product p {
  text-align: center;
  padding: 0 20px;
  margin-bottom: 20px;
  color: #555555;
}

/* About Section */
.about {
  padding: 80px 0;
  background-color: #f9f9f9;
  border-radius: 10px;
  box-shadow: 0 4px 10px rgba(0,0,0,0.1);
  margin: 30px 20px;
}
.about .container {
  max-width: 800px;
  text-align: center;
}
.about h2 {
  color: #0288d1;
  margin-bottom: 30px;
}
.about p {
  font-size: 1.1em;
  line-height: 1.8;
  padding: 0 30px;
  color: #444444;
}

/* Contact Section */
.contact {
  padding: 80px 0;
  background-color: #ffffff;
  border-radius: 10px;
  box-shadow: 0 4px 10px rgba(0,0,0,0.1);
  margin: 30px 20px;
}
.contact .container {
  max-width: 600px;
  text-align: center;
}
.contact h2 {
  color: #0288d1;
  margin-bottom: 30px;
}
.contact p {
  font-size: 1.1em;
  margin-bottom: 20px;
  display: flex;
  justify-content: center;
  align-items: center;
  color: #333333;
}
.contact p::before {
  content: "";
  display: inline-block;
  width: 20px;
  height: 20px;
  background-size: contain;
  background-repeat: no-repeat;
  margin-right: 10px;
}
.contact p:nth-child(2)::before {
  background-image: url('email-icon.png');
}
.contact p:nth-child(3)::before {
  background-image: url('phone-icon.png');
}

  
    </style>
    <header>
      <nav class="navbar">
        <div class="container">
          <a href="#" class="logo">GOODLIFE</a>
          <ul class="nav-links">
            <li><a href="#home">Home</a></li>
            <li><a href="#products">Products</a></li>
            <li><a href="#about">About</a></li>
            <li><a href="#contact">Contact</a></li>
          </ul>
        </div>
      </nav>
    </header>
    <main>
        <section id="home" class="hero">
          <div class="container">
            <h1>LETS SPARKEL WITH GLITTERS AND SHINE</h1>
            <p>GLOW WITH OUR PRODUCTS THAT BOLDS WITH SUNSHINE</p>
            <a href="#products" class="btn">Explore Products</a>
          </div>
        </section>
        <section id="products" class="products">
          <div class="container">
            <h2>Featured Products</h2>
            <div class="product-grid">
              <div class="product">
                <img src="sun.png" alt="MOISTURIZER">
                <h3>Moisturizer with clear</h3>
                <p>Gives you a clear and soft skin.</p>
                <a href="#" class="btn">View Details</a>
              </div>
              <div class="product">
                <img src="sun1.png" alt="SUNSCREEN">
                <h3>SUNSCREEN</h3>
                <p>Immersive SPF sheild of skin.</p>
                <a href="#" class="btn">View Details</a>
              </div>
              <div class="product">
                <img src="sun2.png" alt="SERUM">
                <h3>SERUM WITH GLITERS OF SHINE X</h3>
                <p>This contains a gliters that gives you a shine with spark</p>
                <a href="#" class="btn">View Details</a>
              </div>
            </div>
          </div>
        </section>
        <section id="about" class="about">
          <div class="container">
            <h2>About Twlight</h2>
            <p>We are glad to anounce that our company gives all types of products with dermatologist suggest proved creams and serums for all types of skin.</p>
          </div>
        </section>
        <section id="contact" class="contact">
          <div class="container">
            <h2>Contact Us</h2>
            <p>Email : goodlifetofficial@gmail.com</p>
            <p>Phone : +91 8015809116</p>
          </div>
        </section>
      </main>
      <footer>
        <div class="container">
          <center><p>&copy; 2024 Twlight. All rights reserved.</p></center>
        </div>
      </footer>
     
    </body>

```
## style.css
```

body {
    font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
    margin: 0;
    padding: 0;
    line-height: 1.6;
    background-color: #121212;
    color: #e0e0e0;
  }
  .container {
    max-width: 1200px;
    margin: 0 auto;
    padding: 0 20px;
  }
  .btn {
    display: inline-block;
    background-color: #64b5f6;
    color: #121212;
    padding: 12px 25px;
    text-decoration: none;
    border-radius: 5px;
    transition: background-color 0.3s ease, box-shadow 0.3s ease;
    box-shadow: 0 2px 5px rgba(100, 181, 246, 0.5);
  }
  .btn:hover {
    background-color: #42a5f5;
    box-shadow: 0 4px 10px rgba(100, 181, 246, 0.7);
  }
  .navbar {
    background-color: #1e1e1e;
    padding: 15px 0;
    position: sticky;
    top: 0;
    z-index: 1000;
  }
  .navbar .container {
    display: flex;
    justify-content: space-between;
    align-items: center;
  }
  .navbar .logo {
    font-size: 1.8em;
    font-weight: bold;
    color: #64b5f6;
    text-decoration: none;
  }
  .navbar .nav-links {
    list-style: none;
    display: flex;
  }
  .navbar .nav-links li {
    margin-left: 25px;
  }
  .navbar .nav-links li a {
    color: #e0e0e0;
    text-decoration: none;
    transition: color 0.3s ease;
  }
  .navbar .nav-links li a:hover {
    color: #64b5f6;
  }
  .hero {
    background-image: linear-gradient(rgba(0, 0, 0, 0.6), rgba(0, 0, 0, 0.6)), url('hero-bg.jpg');
    background-size: cover;
    background-position: center;
    color: #e0e0e0;
    text-align: center;
    padding: 150px 0;
  }
  .hero h1 {
    font-size: 3em;
    margin-bottom: 20px;
    text-shadow: 2px 2px 5px rgba(0, 0, 0, 0.8);
  }
  .hero p {
    font-size: 1.2em;
    margin-bottom: 30px;
    text-shadow: 1px 1px 3px rgba(0, 0, 0, 0.6);
  }
  .products {
    padding: 80px 0;
  }
  .products h2 {
    text-align: center;
    margin-bottom: 50px;
    color: #64b5f6;
    text-shadow: 1px 1px 3px rgba(0, 0, 0, 0.6);
  }
  .product-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
    grid-gap: 30px;
  }
  .product {
    background-color: #1e1e1e;
    border-radius: 8px;
    box-shadow: 0 4px 10px rgba(0, 0, 0, 0.3);
    overflow: hidden;
    transition: transform 0.3s ease, box-shadow 0.3s ease;
  }
  .product:hover {
    transform: translateY(-5px);
    box-shadow: 0 6px 15px rgba(0, 0, 0, 0.4);
  }
  .product img {
    width: 100%;
    height: auto;
    display: block;
  }
  .product h3 {
    color: #64b5f6;
    margin: 20px 0 10px;
    text-align: center;
  }
  .product p {
    text-align: center;
    padding: 0 20px;
    margin-bottom: 20px;
  }
  .about {
    padding: 80px 0;
    background-color: #1a1a1a;
    border-radius: 10px;
    box-shadow: 0 4px 10px rgba(0, 0, 0, 0.3);
    margin: 30px 20px;
  }
  .about .container {
    max-width: 800px;
    text-align: center;
  }
  .about h2 {
    color: #64b5f6;
    margin-bottom: 30px;
    text-shadow: 1px 1px 3px rgba(0, 0, 0, 0.6);
  }
  .about p {
    font-size: 1.1em;
    line-height: 1.8;
    padding: 0 30px;
  }
  .contact {
    padding: 80px 0;
    background-color: #222222;
    border-radius: 10px;
    box-shadow: 0 4px 10px rgba(0, 0, 0, 0.3);
    margin: 30px 20px;
  }
  .contact .container {
    max-width: 600px;
    text-align: center;
  }
  .contact h2 {
    color: #64b5f6;
    margin-bottom: 30px;
    text-shadow: 1px 1px 3px rgba(0, 0, 0, 0.6);
  }
  .contact p {
    font-size: 1.1em;
    margin-bottom: 20px;
    display: flex;
    justify-content: center;
    align-items: center;
  }
  .contact p::before {
    content: "";
    display: inline-block;
    width: 20px;
    height: 20px;
    background-size: contain;
    background-repeat: no-repeat;
    margin-right: 10px;
  }
  .contact p:nth-child(2)::before {
    background-image: url('email-icon.png');
  }
  .contact p:nth-child(3)::before {
    background-image: url('phone-icon.png');
  }
  

```
## OUTPUT
<img width="1914" height="1015" alt="Screenshot 2025-08-17 210344" src="https://github.com/user-attachments/assets/c364f7ef-052a-4e75-aac8-8659a00372c3" />

<img width="1912" height="1078" alt="Screenshot 2025-08-17 210400" src="https://github.com/user-attachments/assets/caffcca0-337d-402c-8827-c04d26fe4eb4" />
<img width="1919" height="1079" alt="Screenshot 2025-08-17 210412" src="https://github.com/user-attachments/assets/7b0a9e7c-ffa7-44eb-9568-a78713f3f3e0" />


## RESULT
The program for creating commercial website using CSS Flexbox is executed successfully.
