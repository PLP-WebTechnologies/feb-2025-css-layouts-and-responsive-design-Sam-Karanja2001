# CSS Layouts and Responsive Design

## Objectives

Implement Flexbox and Grid for layout design.
Make the webpage responsive using media queries.
Ensure proper alignment and spacing.

## Instructions

- use Flexbox or CSS Grid.
- Add a navigation bar and structure the content.
- Use media queries to adjust layout for mobile, tablet, and desktop.

>[!NOTE]
>  - Include at least:
>  - navigation bar
>  - media queries

# Tasks

- Apply Flexbox or Grid for layout.
- Make the page responsive.
- Test across different screen sizes.

Happy Coding! 💻✨



HTML Structure

The basic structure for the webpage:

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Responsive Design with Flexbox</title>
    <link rel="stylesheet" href="styles.css">
</head>
<body>
    <header>
        <nav>
            <ul>
                <li><a href="#">Home</a></li>
                <li><a href="#">About</a></li>
                <li><a href="#">Services</a></li>
                <li><a href="#">Contact</a></li>
            </ul>
        </nav>
    </header>

    <main>
        <section class="content">
            <h1>Welcome to Our Website</h1>
            <p>This is a responsive page using Flexbox.</p>
        </section>

        <section class="features">
            <div class="feature">Feature 1</div>
            <div class="feature">Feature 2</div>
            <div class="feature">Feature 3</div>
        </section>
    </main>

    <footer>
        <p>Footer Content</p>
    </footer>
</body>
</html>

CSS with Flexbox and Media Queries

/* General Styles */
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}

body {
    font-family: Arial, sans-serif;
}

header {
    background-color: #333;
    color: white;
    padding: 10px 0;
}

nav ul {
    display: flex;
    justify-content: center;
    list-style: none;
}

nav ul li {
    margin: 0 20px;
}

nav ul li a {
    color: white;
    text-decoration: none;
    font-size: 18px;
}

main {
    padding: 20px;
}

.content {
    text-align: center;
    margin-bottom: 20px;
}

.features {
    display: flex;
    justify-content: space-around;
    gap: 20px;
}

.feature {
    background-color: #f4f4f4;
    padding: 20px;
    border-radius: 8px;
    width: 30%;
    text-align: center;
}

footer {
    background-color: #333;
    color: white;
    text-align: center;
    padding: 10px 0;
}

/* Media Queries for Responsiveness */
@media (max-width: 768px) {
    nav ul {
        flex-direction: column;
    }

    .features {
        flex-direction: column;
        align-items: center;
    }

    .feature {
        width: 80%;
        margin-bottom: 20px;
    }
}

@media (max-width: 480px) {
    .feature {
        width: 100%;
    }

    nav ul {
        padding: 0;
    }
}



