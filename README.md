# CSS-assignment
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Responsive Layout</title>
    <link rel="stylesheet" href="styles.css">
</head>
<body>
    <header>
        <nav>
            <div class="logo">Logo</div>
            <div class="hamburger-menu" id="hamburger-menu">☰</div>
            <ul class="nav-links" id="nav-links">
                <li><a href="#">Home</a></li>
                <li><a href="#">About</a></li>
                <li><a href="#">Services</a></li>
                <li><a href="#">Contact</a></li>
            </ul>
        </nav>
    </header>
    <div class="container">
        <aside class="sidebar" id="sidebar">
            <ul>
                <li><a href="#">Link 1</a></li>
                <li><a href="#">Link 2</a></li>
                <li><a href="#">Link 3</a></li>
            </ul>
        </aside>
        <main class="main-content">
            <h1>Welcome to the Responsive Layout</h1>
            <p>This is the main content area.</p>
        </main>
    </div>
    <script src="script.js"></script>
</body>
</html>

body {
    font-family: Arial, sans-serif;
    margin: 0;
    padding: 0;
}

header {
    background-color: #333;
    color: white;
    padding: 1rem;
}

nav {
    display: flex;
    justify-content: space-between;
    align-items: center;
}

.nav-links {
    list-style: none;
    display: flex;
    gap: 1rem;
}

.nav-links li a {
    color: white;
    text-decoration: none;
}

.hamburger-menu {
    display: none;
    font-size: 2rem;
    cursor: pointer;
}

.container {
    display: flex;
    flex-wrap: wrap;
}

.sidebar {
    flex: 1;
    background-color: #f4f4f4;
    padding: 1rem;
}

.main-content {
    flex: 3;
    padding: 1rem;
}

@media (max-width: 768px) {
    .nav-links {
        display: none;
        flex-direction: column;
    }

    .hamburger-menu {
        display: block;
    }

    .container {
        flex-direction: column;
    }

    .sidebar {
        order: 2;
    }

    .main-content {
        order: 1;
    }
}
