<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Healix Care - Admin Panel</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        /* Global Styles */
        :root {
            --primary: #2c3e50;
            --secondary: #3498db;
            --accent: #e74c3c;
            --light: #ecf0f1;
            --dark: #2c3e50;
            --success: #2ecc71;
        }
        
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        }
        
        body {
            background-color: #f9f9f9;
            color: #333;
            line-height: 1.6;
        }
        
        .container {
            width: 90%;
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 15px;
        }
        
        .btn {
            display: inline-block;
            background: var(--secondary);
            color: white;
            padding: 10px 20px;
            border: none;
            border-radius: 4px;
            cursor: pointer;
            text-decoration: none;
            font-size: 16px;
            transition: all 0.3s ease;
        }
        
        .btn:hover {
            background: #2980b9;
            transform: translateY(-2px);
        }
        
        .btn-danger {
            background: var(--accent);
        }
        
        .btn-danger:hover {
            background: #c0392b;
        }
        
        .btn-success {
            background: var(--success);
        }
        
        .btn-success:hover {
            background: #27ae60;
        }
        
        /* Header Styles */
        header {
            background-color: var(--primary);
            color: white;
            padding: 15px 0;
            box-shadow: 0 2px 10px rgba(0,0,0,0.1);
        }
        
        .header-content {
            display: flex;
            justify-content: space-between;
            align-items: center;
        }
        
        .logo {
            display: flex;
            align-items: center;
        }
        
        .logo-img {
            height: 50px;
            margin-right: 10px;
        }
        
        .logo h1 {
            font-size: 24px;
            background: linear-gradient(45deg, #3498db, #2ecc71);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            font-weight: 700;
        }
        
        nav ul {
            display: flex;
            list-style: none;
        }
        
        nav ul li {
            margin-left: 20px;
        }
        
        nav ul li a {
            color: white;
            text-decoration: none;
            font-weight: 500;
            transition: color 0.3s;
        }
        
        nav ul li a:hover {
            color: var(--secondary);
        }
        
        /* Admin Panel */
        .admin-panel {
            background: white;
            border-radius: 8px;
            padding: 30px;
            box-shadow: 0 5px 15px rgba(0,0,0,0.1);
            margin: 40px 0;
        }
        
        .admin-panel h2 {
            color: var(--primary);
            margin-bottom: 20px;
            padding-bottom: 10px;
            border-bottom: 1px solid #eee;
        }
        
        .form-group {
            margin-bottom: 20px;
        }
        
        .form-group label {
            display: block;
            margin-bottom: 8px;
            font-weight: 500;
        }
        
        .form-control {
            width: 100%;
            padding: 10px 15px;
            border: 1px solid #ddd;
            border-radius: 4px;
            font-size: 16px;
        }
        
        textarea.form-control {
            min-height: 120px;
            resize: vertical;
        }
        
        /* Admin Login */
        .admin-login {
            max-width: 400px;
            margin: 50px auto;
            background: white;
            padding: 30px;
            border-radius: 8px;
            box-shadow: 0 5px 15px rgba(0,0,0,0.1);
        }
        
        .admin-login h2 {
            text-align: center;
            margin-bottom: 20px;
            color: var(--primary);
        }
        
        /* Footer */
        footer {
            background: var(--primary);
            color: white;
            padding: 30px 0;
            margin-top: 50px;
        }
        
        .copyright {
            text-align: center;
            color: #bbb;
            font-size: 14px;
        }
    </style>
</head>
<body>
    <!-- Header -->
    <header>
        <div class="container">
            <div class="header-content">
                <div class="logo">
                    <div class="logo-img">
                        <svg width="50" height="50" viewBox="0 0 50 50">
                            <circle cx="25" cy="25" r="20" fill="#3498db" opacity="0.8"/>
                            <path d="M25,10 L30,20 L40,22 L32,30 L34,40 L25,35 L16,40 L18,30 L10,22 L20,20 Z" fill="#2ecc71"/>
                            <circle cx="25" cy="25" r="8" fill="#2c3e50"/>
                        </svg>
                    </div>
                    <h1>Healix Care - Admin</h1>
                </div>
                <nav>
                    <ul>
                        <li><a href="index.html">Back to Website</a></li>
                        <li><a href="#" id="admin-logout">Logout</a></li>
                    </ul>
                </nav>
            </div>
        </div>
    </header>

    <!-- Admin Login -->
    <section id="admin-login-page">
        <div class="container">
            <div class="admin-login">
                <h2>Admin Login</h2>
                <form id="admin-login-form">
                    <div class="form-group">
                        <label for="admin-username">Username</label>
                        <input type="text" id="admin-username" class="form-control" required>
                    </div>
                    <div class="form-group">
                        <label for="admin-password">Password</label>
                        <input type="password" id="admin-password" class="form-control" required>
                    </div>
                    <button type="submit" class="btn" style="width: 100%;">Login</button>
                </form>
            </div>
        </div>
    </section>

    <!-- Admin Panel -->
    <section id="admin-page" style="display: none;">
        <div class="container">
            <div class="admin-panel">
                <div style="display: flex; justify-content: space-between; align-items: center; margin-bottom: 20px;">
                    <h2>Admin Panel - Manage Products</h2>
                    <button class="btn btn-danger" id="admin-logout-btn">Logout</button>
                </div>
                <form id="product-form">
                    <div class="form-group">
                        <label for="product-name">Product Name</label>
                        <input type="text" id="product-name" class="form-control" required>
                    </div>
                    <div class="form-group">
                        <label for="product-description">Description</label>
                        <textarea id="product-description" class="form-control" required></textarea>
                    </div>
                    <div class="form-group">
                        <label for="product-price">Price ($)</label>
                        <input type="number" id="product-price" class="form-control" step="0.01" required>
                    </div>
                    <div class="form-group">
                        <label for="product-image">Image URL</label>
                        <input type="url" id="product-image" class="form-control" required>
                    </div>
                    <div class="form-group">
                        <label for="product-category">Category</label>
                        <select id="product-category" class="form-control" required>
                            <option value="screen-protector">Screen Protector</option>
                            <option value="phone-case">Phone Case</option>
                            <option value="cable">Cable</option>
                            <option value="charger">Charger</option>
                            <option value="other">Other</option>
                        </select>
                    </div>
                    <div class="form-group">
                        <label>
                            <input type="checkbox" id="product-featured">
                            <span>Featured Product</span>
                        </label>
                    </div>
                    <button type="submit" class="btn btn-success">Add Product</button>
                    <button type="button" class="btn btn-danger" id="cancel-edit" style="display: none;">Cancel</button>
                </form>
                
                <div class="existing-products" style="margin-top: 40px;">
                    <h3>Existing Products</h3>
                    <div id="admin-products-list">
                        <!-- Admin product list will be populated here -->
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Footer -->
    <footer>
        <div class="container">
            <div class="copyright">
                <p>&copy; 2023 Healix Care. All rights reserved.</p>
            </div>
        </div>
    </footer>

    <script>
        // Sample products data
        let products = [
            {
                id: 1,
                name: "Tempered Glass Screen Protector",
                description: "9H hardness tempered glass with oleophobic coating to resist fingerprints.",
                price: 12.99,
                image: "https://images.unsplash.com/photo-1601593346740-925612772716?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=687&q=80",
                category: "screen-protector",
                featured: true
            },
            {
                id: 2,
                name: "Silicone Phone Case",
                description: "Shock-absorbent silicone case with raised edges for screen protection.",
                price: 18.99,
                image: "https://images.unsplash.com/photo-1556656793-08538906a9f8?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=1170&q=80",
                category: "phone-case",
                featured: true
            }
        ];

        // Admin credentials
        const adminCredentials = {
            username: "admin",
            password: "healix2023"
        };

        let editingProductId = null;
        let isAdminLoggedIn = false;

        // DOM elements
        const adminLoginPage = document.getElementById('admin-login-page');
        const adminPage = document.getElementById('admin-page');
        const adminLoginForm = document.getElementById('admin-login-form');
        const adminLogoutBtn = document.getElementById('admin-logout-btn');
        const adminProductsList = document.getElementById('admin-products-list');
        const productForm = document.getElementById('product-form');
        const cancelEditBtn = document.getElementById('cancel-edit');

        // Initialize the page
        document.addEventListener('DOMContentLoaded', function() {
            // Check if user is already logged in
            if (localStorage.getItem('adminLoggedIn') === 'true') {
                isAdminLoggedIn = true;
                showAdminPanel();
            }
            
            // Set up admin login form
            adminLoginForm.addEventListener('submit', function(e) {
                e.preventDefault();
                const username = document.getElementById('admin-username').value;
                const password = document.getElementById('admin-password').value;
                
                if (username === adminCredentials.username && password === adminCredentials.password) {
                    isAdminLoggedIn = true;
                    localStorage.setItem('adminLoggedIn', 'true');
                    showAdminPanel();
                } else {
                    alert('Invalid username or password');
                }
            });
            
            // Set up admin logout
            adminLogoutBtn.addEventListener('click', function() {
                isAdminLoggedIn = false;
                localStorage.removeItem('adminLoggedIn');
                showLoginPage();
            });
            
            // Set up product form submission
            productForm.addEventListener('submit', function(e) {
                e.preventDefault();
                
                const productData = {
                    name: document.getElementById('product-name').value,
                    description: document.getElementById('product-description').value,
                    price: parseFloat(document.getElementById('product-price').value),
                    image: document.getElementById('product-image').value,
                    category: document.getElementById('product-category').value,
                    featured: document.getElementById('product-featured').checked
                };
                
                if (editingProductId) {
                    // Update existing product
                    updateProduct(editingProductId, productData);
                } else {
                    // Add new product
                    addProduct(productData);
                }
                
                // Reset form
                productForm.reset();
                cancelEditBtn.style.display = 'none';
                editingProductId = null;
            });
            
            // Set up cancel edit button
            cancelEditBtn.addEventListener('click', function() {
                productForm.reset();
                this.style.display = 'none';
                editingProductId = null;
            });
            
            // Render products
            renderAdminProducts();
        });

        // Show admin panel
        function showAdminPanel() {
            adminLoginPage.style.display = 'none';
            adminPage.style.display = 'block';
        }

        // Show login page
        function showLoginPage() {
            adminLoginPage.style.display = 'block';
            adminPage.style.display = 'none';
        }

        // Render products in admin panel
        function renderAdminProducts() {
            adminProductsList.innerHTML = '';
            
            products.forEach(product => {
                const productItem = document.createElement('div');
                productItem.className = 'admin-product-item';
                productItem.style.cssText = `
                    display: flex;
                    justify-content: space-between;
                    align-items: center;
                    padding: 15px;
                    border: 1px solid #eee;
                    border-radius: 4px;
                    margin-bottom: 10px;
                `;
                productItem.innerHTML = `
                    <div>
                        <h4>${product.name}</h4>
                        <p>$${product.price.toFixed(2)}</p>
                    </div>
                    <div>
                        <button class="btn edit-product" data-id="${product.id}">Edit</button>
                        <button class="btn btn-danger delete-product" data-id="${product.id}">Delete</button>
                    </div>
                `;
                adminProductsList.appendChild(productItem);
            });
            
            // Add event listeners to edit and delete buttons
            document.querySelectorAll('.edit-product').forEach(button => {
                button.addEventListener('click', function() {
                    const productId = parseInt(this.getAttribute('data-id'));
                    editProduct(productId);
                });
            });
            
            document.querySelectorAll('.delete-product').forEach(button => {
                button.addEventListener('click', function() {
                    const productId = parseInt(this.getAttribute('data-id'));
                    deleteProduct(productId);
                });
            });
        }

        // Add a new product
        function addProduct(productData) {
            const newProduct = {
                id: products.length > 0 ? Math.max(...products.map(p => p.id)) + 1 : 1,
                ...productData
            };
            
            products.push(newProduct);
            renderAdminProducts();
            alert('Product added successfully!');
        }

        // Edit a product
        function editProduct(productId) {
            const product = products.find(p => p.id === productId);
            if (product) {
                document.getElementById('product-name').value = product.name;
                document.getElementById('product-description').value = product.description;
                document.getElementById('product-price').value = product.price;
                document.getElementById('product-image').value = product.image;
                document.getElementById('product-category').value = product.category;
                document.getElementById('product-featured').checked = product.featured;
                
                editingProductId = productId;
                cancelEditBtn.style.display = 'inline-block';
            }
        }

        // Update a product
        function updateProduct(productId, productData) {
            const productIndex = products.findIndex(p => p.id === productId);
            if (productIndex !== -1) {
                products[productIndex] = { id: productId, ...productData };
                renderAdminProducts();
                alert('Product updated successfully!');
            }
        }

        // Delete a product
        function deleteProduct(productId) {
            if (confirm('Are you sure you want to delete this product?')) {
                products = products.filter(p => p.id !== productId);
                renderAdminProducts();
                alert('Product deleted successfully!');
            }
        }
    </script>
</body>
</html>
