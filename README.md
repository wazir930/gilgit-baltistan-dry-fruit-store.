baltistani-dry-fruit-store/
│
├── index.html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Baltistani Dry Fruit Store</title>
  <link rel="stylesheet" href="styles.css">
  <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0/css/all.min.css">
</head>
<body>
  <!-- Header Section -->
  <header>
    <div class="logo">
      <img src="images/logo.png" alt="Baltistani Dry Fruit Store Logo">
    </div>
    <nav>
      <ul>
        <li><a href="#home">Home</a></li>
        <li><a href="#products">Products</a></li>
        <li><a href="#about">About Us</a></li>
        <li><a href="#contact">Contact</a></li>
      </ul>
    </nav>
    <div class="cart">
      <i class="fas fa-shopping-cart"></i>
      <span class="cart-count">0</span>
    </div>
  </header>

  <!-- Hero Section -->
  <section id="home" class="hero">
    <h1>Welcome to Baltistani Dry Fruit Store</h1>
    <p>Healthy, Natural, and Delicious Dry Fruits from the Heart of Baltistan!</p>
    <a href="#products" class="btn">Shop Now</a>
  </section>

  <!-- Products Section -->
  <section id="products" class="products">
    <h2>Our Products</h2>
    <div class="product-grid">
      <div class="product-card">
        <img src="images/almonds.jpg" alt="Almonds">
        <h3>Almonds</h3>
        <p>$10 per kg</p>
        <button class="add-to-cart" data-name="Almonds" data-price="10">Add to Cart</button>
      </div>
      <div class="product-card">
        <img src="images/walnuts.jpg" alt="Walnuts">
        <h3>Walnuts</h3>
        <p>$12 per kg</p>
        <button class="add-to-cart" data-name="Walnuts" data-price="12">Add to Cart</button>
      </div>
      <div class="product-card">
        <img src="images/cashews.jpg" alt="Cashews">
        <h3>Cashews</h3>
        <p>$15 per kg</p>
        <button class="add-to-cart" data-name="Cashews" data-price="15">Add to Cart</button>
      </div>
    </div>
  </section>

  <!-- Shopping Cart Modal -->
  <div id="cart-modal" class="modal">
    <div class="modal-content">
      <span class="close">&times;</span>
      <h2>Your Cart</h2>
      <ul id="cart-items"></ul>
      <p>Total: $<span id="cart-total">0</span></p>
      <button id="checkout">Checkout</button>
    </div>
  </div>

  <!-- About Us Section -->
  <section id="about" class="about">
    <h2>About Us</h2>
    <p>We are passionate about providing the best quality dry fruits sourced directly from the fertile valleys of Baltistan. Our products are 100% natural and packed with nutrients.</p>
  </section>

  <!-- Contact Section -->
  <section id="contact" class="contact">
    <h2>Contact Us</h2>
    <form>
      <input type="text" placeholder="Your Name" required>
      <input type="email" placeholder="Your Email" required>
      <textarea placeholder="Your Message" required></textarea>
      <button type="submit">Send Message</button>
    </form>
  </section>

  <!-- Footer -->
  <footer>
    <p>&copy; 2023 Baltistani Dry Fruit Store. All rights reserved.</p>
    <div class="social-icons">
      <a href="#"><i class="fab fa-facebook"></i></a>
      <a href="#"><i class="fab fa-instagram"></i></a>
      <a href="#"><i class="fab fa-twitter"></i></a>
    </div>
  </footer>

  <script src="script.js"></script>
</body>
</html>
├── styles.css
/* General Styles */
body {
  font-family: Arial, sans-serif;
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

header {
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 20px;
  background-color: #f8f8f8;
  border-bottom: 1px solid #ddd;
  position: sticky;
  top: 0;
  z-index: 1000;
}

.logo img {
  height: 50px;
}

nav ul {
  list-style: none;
  display: flex;
  gap: 20px;
}

nav a {
  text-decoration: none;
  color: #333;
}

.cart {
  position: relative;
  cursor: pointer;
}

.cart-count {
  position: absolute;
  top: -10px;
  right: -10px;
  background-color: red;
  color: white;
  border-radius: 50%;
  padding: 2px 6px;
  font-size: 12px;
}

.hero {
  background: url('images/hero-bg.jpg') no-repeat center center/cover;
  color: white;
  text-align: center;
  padding: 100px 20px;
}

.hero h1 {
  font-size: 3rem;
  animation: fadeIn 2s;
}

.hero p {
  font-size: 1.5rem;
  animation: fadeIn 3s;
}

.btn {
  background-color: #ff6f61;
  color: white;
  padding: 10px 20px;
  text-decoration: none;
  border-radius: 5px;
  animation: bounce 2s infinite;
}

@keyframes fadeIn {
  from { opacity: 0; }
  to { opacity: 1; }
}

@keyframes bounce {
  0%, 100% { transform: translateY(0); }
  50% { transform: translateY(-10px); }
}

.products {
  padding: 50px 20px;
  text-align: center;
}

.product-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
  gap: 20px;
}

.product-card {
  border: 1px solid #ddd;
  padding: 20px;
  border-radius: 10px;
  text-align: center;
  transition: transform 0.3s;
}

.product-card:hover {
  transform: scale(1.05);
}

.product-card img {
  width: 100%;
  height: auto;
  border-radius: 10px;
}

.add-to-cart {
  background-color: #ff6f61;
  color: white;
  border: none;
  padding: 10px 20px;
  border-radius: 5px;
  cursor: pointer;
}

.modal {
  display: none;
  position: fixed;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background-color: rgba(0, 0, 0, 0.5);
  justify-content: center;
  align-items: center;
}

.modal-content {
  background-color: white;
  padding: 20px;
  border-radius: 10px;
  width: 300px;
  text-align: center;
}

.close {
  float: right;
  cursor: pointer;
}

footer {
  background-color: #333;
  color: white;
  text-align: center;
  padding: 20px;
}

.social-icons {
  margin-top: 10px;
}

.social-icons a {
  color: white;
  margin: 0 10px;
  font-size: 1.2rem;
}
├── script.js
// Shopping Cart Logic
const cartButtons = document.querySelectorAll('.add-to-cart');
const cartCount = document.querySelector('.cart-count');
const cartModal = document.getElementById('cart-modal');
const closeModal = document.querySelector('.close');
const cartItemsList = document.getElementById('cart-items');
const cartTotal = document.getElementById('cart-total');
const checkoutButton = document.getElementById('checkout');

let cart = [];
let total = 0;

// Add to Cart
cartButtons.forEach(button => {
  button.addEventListener('click', () => {
    const name = button.getAttribute('data-name');
    const price = parseFloat(button.getAttribute('data-price'));
    cart.push({ name, price });
    total += price;
    updateCart();
  });
});

// Update Cart
function updateCart() {
  cartCount.textContent = cart.length;
  cartItemsList.innerHTML = '';
  cart.forEach(item => {
    const li = document.createElement('li');
    li.textContent = `${item.name} - $${item.price}`;
    cartItemsList.appendChild(li);
  });
  cartTotal.textContent = total.toFixed(2);
}

// Open Cart Modal
document.querySelector('.cart').addEventListener('click', () => {
  cartModal.style.display = 'flex';
});

// Close Cart Modal
closeModal.addEventListener('click', () => {
  cartModal.style.display = 'none';
});

// Checkout
checkoutButton.addEventListener('click', () => {
  alert(`Thank you for your purchase! Total: $${total.toFixed(2)}`);
  cart = [];
  total = 0;
  updateCart();
  cartModal.style.display = 'none';
});
├── images/ (store all your images here)
├── index.html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>My Vercel Website</title>
    <link rel="stylesheet" href="styles.css">
</head>
<body>

    justify-content: center;
    background-color: #fff; /* Optional: dark blue and green */
    padding: 10px; /* Optional: Add some padding */
}

