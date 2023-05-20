<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Home-The Grocery Shop</title>
    <script src="https://unpkg.com/typed.js@2.0.16/dist/typed.umd.js"></script>
    <style> @import url('https://fonts.googleapis.com/css2?family=Roboto+Mono:wght@100&display=swap');
@import url('https://fonts.googleapis.com/css2?family=Roboto+Mono:wght@100&display=swap');
*{
    margin: 0%;
    padding: 0%;
}
body{
    background: rgb(168, 219, 202);
}
nav ul{
    display: flex;
    list-style: none;
    height: 40px;
    background-color: black;
    color: aliceblue;
    margin-bottom: 5%;
}
nav ul li{
    display: flex;
    padding: 1%; 
    align-items: center
    
}
nav ul li a{
    text-decoration: none;
    color: rgb(251, 251, 251);
    
}
nav ul li a:hover{
    text-decoration: none;
    color: rgb(105, 169, 98);
    font-size: 1.2rem;
    
}
nav ul li:last-child{
   display: flexbox;
    text-align: right;
    padding-left: 82%;
}
div{
    display: inline-block;    
    padding-left: 3em;
    color: rgb(34, 62, 63);
    font-size: 30px;
    margin: 2px 10;
}
div b{
    color: rgb(51, 54, 54);
}
#element{
    color: rgb(51, 54, 54); 
}
hr{
     
}

/* Add your CSS styles here */
body {
    font-family: Arial, sans-serif;
    margin: 0;
    padding: 0;
  }
  header {
    background-color: #333;
    color: white;
    padding: 20px;
    text-align: center;
  }
  header a {
    color: white;
    text-decoration: none;
  }
  .container {
    max-width: 1200px;
    margin: 0 auto;
    padding: 20px;
  }
  .product-list {
    display: flex;
    flex-wrap: wrap;
    justify-content: space-between;
  }
  .product {
    width: 30%;
    margin-bottom: 20px;
  }
  .product img {
    width: 100%;
    height: auto;
  }
  .product h3 {
    font-size: 1.2em;
    margin: 10px 0;
  }
  .product p {
    color: #777;
    margin: 10px 0;
  }
  .product .price {
    color: #333;
    font-size: 1.2em;
    font-weight: bold;
    margin: 10px 0;
  }
  .product button {
    background-color: #333;
    border: none;
    color: white;
    cursor: pointer;
    font-size: 1em;
    padding: 10px;
    width: 100%;
  }
  .product button:hover {
    background-color: #444;
  }
  footer {
    background-color: #333;
    color: white;
    padding: 20px;
    text-align: center;
  }
<style>
</head>

<body>
    <nav>
        <ul>
            <li> <a href="https://www.google.com/">Home</a></li>
            <li> <a href="https://www.google.com/">About</a></li>
            <li> <a href="https://www.google.com/">Contact</a></li>
            <li> <a href="https://www.google.com/">Help</a></li>
        </ul>
    </nav>

    <div class="element">Hii, Welcome to our <b id="color">Shop</b><br> we are in the town <br> with a <b><span
                id="element"></span></b>
    </div>

    
    <!-- <section class="secondsection">
        <div>Our products</div>
    </section> -->

    <header>
        <a href="#">Our Product</a>
      </header>
      <div class="container">
        <div class="product-list">
          <!-- Add your products here -->
          <div class="product">
            <img src="Grocery-PNG.png" alt="Product Image">
            <h3>Grocery</h3>
            <p>Fruits, vegetables, and herbs are essential components of a balanced diet. They are typically sourced from local farms or imported from other regions.</p>
            <div class="price">$49.99</div>
            <button>Add to Cart</button>
          </div>
          <div class="product">
            <img src="style png.jpg" alt="Product Image">
            <h3>style</h3>
            <p>This category encompasses a wide range of apparel, including shirts, pants, dresses, skirts, jackets, and more. Different styles, sizes, and materials are available to suit individual preferences.</p>
            <div class="price">$49.99</div>
            <button>Add to Cart</button>
          </div>
          <div class="product">
            <img src="sports png.png" alt="Product Image">
            <h3>sports</h3>
            <p>Clothing specifically designed for sports activities, such as jerseys, shorts, leggings, athletic shoes, and performance fabrics.</p>
            <div class="price">$49.99</div>
            <button>Add to Cart</button>
          </div>
            <script>
                // Add your JavaScript code here
                // This example adds a "Add to Cart" button event listener to each product
                document.addEventListener("DOMContentLoaded", function() {
                  const products = document.querySelectorAll(".product");
                  products.forEach(function(product) {
                    const button = product.querySelector("button");
                    button.addEventListener("click", function() {
                      // Add product to cart
                      alert("Product added to cart!");
                    });
                  });
                });
              </script>
              
            <script>
                // Add your JavaScript code here
                // This example adds a "Add to Cart" button event listener to each product
                document.addEventListener("DOMContentLoaded", function() {
                  const products = document.querySelectorAll(".product");
                  products.forEach(function(product) {
                    const button = product.querySelector("button");
                    button.addEventListener("click", function() {
                      // Add product to cart
                      addToCart(product);
                    });
                  });
                });
              
                // This function adds a product to the cart
                function addToCart(product) {
                  // Get product details
                  const name = product.querySelector("h3").textContent;
                  const price = product.querySelector(".price").textContent;
              
                  // Add product to cart
                  const cart = document.querySelector(".cart");
                  const cartItem = document.createElement("div");
                  cartItem.classList.add("cart-item");
                  cartItem.innerHTML = `
                    <h3>${name}</h3>
                    <p>${price}</p>
                    <button>Remove</button>
                  `;
                  cart.appendChild(cartItem);
              
                  // Add event listener to remove button
                  const removeButton = cartItem.querySelector("button");
                  removeButton.addEventListener("click", function() {
                    cartItem.remove();
                  });
              
                  // Update total
                  updateTotal();
                }
              
                // This function updates the total price of the items in the cart
                function updateTotal() {
                  const cart = document.querySelector(".cart");
                  const items = cart.querySelectorAll(".cart-item");
                  let total = 0;
                  items.forEach(function(item) {
                    const price = item.querySelector("p").textContent;
                    total += parseFloat(price.substring(1));
                  });
                  document.querySelector(".total").textContent = `Total: $${total.toFixed(2)}`;
                }
              </script>
              
           <hr>
    <script src="home_shop.js"></script>
</body>

</html>
