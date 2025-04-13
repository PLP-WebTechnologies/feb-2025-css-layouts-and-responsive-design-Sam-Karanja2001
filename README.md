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

  <!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Responsive Layout with Grid</title>
    <style>
        body {
            font-family: sans-serif;
            margin: 0;
            padding: 0;
            background-color: #f4f4f4;
            color: #333;
        }

        /* Navigation Bar */
        nav {
            background-color: #333;
            color: white;
            padding: 1em;
        }

        nav ul {
            list-style: none;
            padding: 0;
            margin: 0;
            display: grid; /* Using CSS Grid for navigation */
            grid-template-columns: repeat(auto-fit, minmax(100px, 1fr)); /* Distribute items evenly */
            gap: 10px;
        }

        nav a {
            color: white;
            text-decoration: none;
            padding: 0.5em 1em;
            text-align: center;
        }

        /* Main Content (using CSS Grid) */
        .container {
            display: grid;
            grid-template-columns: 1fr 300px; /* Two columns: main content and sidebar */
            gap: 20px;
            padding: 20px;
        }

        main {
            background-color: white;
            padding: 20px;
            border-radius: 8px;
        }

        aside {
            background-color: #ddd;
            padding: 20px;
            border-radius: 8px;
        }

        footer {
            background-color: #333;
            color: white;
            text-align: center;
            padding: 1em;
            grid-column: 1 / -1; /* Make footer span across all grid columns */
        }

        /* Media Queries for Responsive Design */

        /* Mobile View (up to 600px width) */
        @media (max-width: 600px) {
            nav ul {
                grid-template-columns: 1fr; /* Stack navigation items vertically */
            }

            .container {
                grid-template-columns: 1fr; /* Stack main and sidebar vertically */
            }
        }

        /* Tablet View (601px to 1024px width) */
        @media (min-width: 601px) and (max-width: 1024px) {
            .container {
                grid-template-columns: 1fr 1fr; /* Two equal columns for main and sidebar */
            }
        }

        /* Desktop View (1025px and above) */
        @media (min-width: 1025px) {
            .container {
                grid-template-columns: 3fr 1fr; /* Main content takes 3/4, sidebar takes 1/4 */
            }
        }
    </style>
</head>
<body>

    <nav>
        <ul>
            <li><a href="#">Home</a></li>
            <li><a href="#">About</a></li>
            <li><a href="#">Services</a></li>
            <li><a href="#">Contact</a></li>
        </ul>
    </nav>

    <div class="container">
        <main>
            <h2>Main Content</h2>
            <p>This is the main content area of the webpage. We are using CSS Grid to structure the layout, providing powerful two-dimensional layout capabilities. This section will contain the primary information and features of the page.</p>
            <p>Grid allows us to define rows and columns, making it easy to position and align elements. Notice how the sidebar moves below this content on smaller screens due to the media queries, and how it might appear next to the content on larger screens.</p>
            <ul>
                <li>Item A</li>
                <li>Item B</li>
                <li>Item C</li>
            </ul>
        </main>

        <aside>
            <h3>Sidebar</h3>
            <p>This is the sidebar content. It can contain related information, advertisements, navigation links, or other supplementary content.</p>
            <ul>
                <li>Link 1</li>
                <li>Link 2</li>
                <li>Link 3</li>
            </ul>
        </aside>
    </div>

    <footer>
        <p>&copy; 2025 Responsive Layout with Grid</p>
    </footer>

</body>
</html>  
