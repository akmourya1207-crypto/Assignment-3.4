Below is the non-semantic (div-based) "Before" version alongside the updated Semantic HTML5 "After" version (index.html).

1. Before Code (before.html — Non-Semantic Version)
This represents the unorganized div-based HTML structure prior to adding semantic tags:

HTML
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Tech Insights Blog - Before</title>
</head>
<body>
    <!-- Header -->
    <div id="header">
        <div class="logo"><h1>Tech Insights</h1></div>
        <div id="nav">
            <a href="#home">Home</a> | 
            <a href="#articles">Articles</a> | 
            <a href="#about">About Us</a> | 
            <a href="#contact">Contact</a>
        </div>
    </div>

    <!-- Main Content Area -->
    <div id="main-content">
        <!-- Main Article Section -->
        <div class="content">
            <div class="article">
                <h2>Understanding Semantic HTML5</h2>
                <div class="meta">Published on October 22, 2026 by Jane Doe</div>
                <!-- Missing alt text on image -->
                <img src="https://via.placeholder.com/600x300" title="code snippet">
                <p>Semantic HTML introduces elements that clearly describe their meaning to both the browser and the developer...</p>
            </div>

            <div class="article">
                <h2>Why Accessibility (a11y) Matters</h2>
                <div class="meta">Published on October 18, 2026 by John Smith</div>
                <p>Web accessibility ensures that websites, tools, and technologies are designed and developed so that people with disabilities can use them...</p>
            </div>
        </div>

        <!-- Sidebar Area -->
        <div id="sidebar">
            <h3>Related Resources</h3>
            <div class="links">
                <a href="#">MDN Web Docs</a><br>
                <a href="#">W3C Web Accessibility Initiative</a>
            </div>
        </div>
    </div>

    <!-- Footer -->
    <div id="footer">
        <p>&copy; 2026 Tech Insights. All rights reserved.</p>
    </div>
</body>
</html>
2. After Code (index.html — Updated Semantic & Accessible Version)
This is your final converted submission file using HTML5 semantic elements (<header>, <nav>, <main>, <section>, <article>, <aside>, <footer>), correct heading hierarchy, accessible images, and proper navigation wrappers.

HTML
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Tech Insights Blog - Semantic HTML & Accessibility</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            line-height: 1.6;
            margin: 0;
            padding: 0;
            color: #333;
            background-color: #f9f9f9;
        }
        header {
            background-color: #1a2a3a;
            color: #fff;
            padding: 1rem 2rem;
            display: flex;
            justify-content: space-between;
            align-items: center;
        }
        header h1 {
            margin: 0;
            font-size: 1.8rem;
        }
        nav ul {
            list-style: none;
            margin: 0;
            padding: 0;
            display: flex;
            gap: 15px;
        }
        nav a {
            color: #fff;
            text-decoration: none;
            font-weight: bold;
        }
        nav a:hover, nav a:focus {
            text-decoration: underline;
            outline: 2px solid #ffbf00;
        }
        .container {
            display: flex;
            max-width: 1100px;
            margin: 20px auto;
            padding: 0 20px;
            gap: 30px;
        }
        main {
            flex: 3;
        }
        aside {
            flex: 1;
            background-color: #eef2f5;
            padding: 20px;
            border-radius: 5px;
            height: fit-content;
        }
        article {
            background: #fff;
            padding: 20px;
            margin-bottom: 20px;
            border-radius: 5px;
            box-shadow: 0 2px 5px rgba(0,0,0,0.1);
        }
        article img {
            max-width: 100%;
            height: auto;
            border-radius: 4px;
            margin-top: 10px;
        }
        .meta {
            font-size: 0.9rem;
            color: #666;
            margin-bottom: 15px;
        }
        footer {
            text-align: center;
            padding: 20px;
            background-color: #1a2a3a;
            color: #fff;
            margin-top: 40px;
        }
    </style>
</head>
<body>

    <!-- Step 1 & 2: Header and Navigation inside <nav> -->
    <header>
        <h1>Tech Insights</h1>
        <nav aria-label="Main Navigation">
            <ul>
                <li><a href="#home">Home</a></li>
                <li><a href="#articles">Articles</a></li>
                <li><a href="#about">About Us</a></li>
                <li><a href="#contact">Contact</a></li>
            </ul>
        </nav>
    </header>

    <div class="container">
        <!-- Step 1 & 3: Main content wrapper -->
        <main id="main-content">
            
            <section id="articles">
                <!-- Step 4: Correct Heading Hierarchy (h1 in header, h2 for section, h3 for article titles) -->
                <h2>Latest Articles</h2>

                <!-- Article 1 -->
                <article>
                    <h3>Understanding Semantic HTML5</h3>
                    <p class="meta">Published on <time datetime="2026-10-22">October 22, 2026</time> by <span>Jane Doe</span></p>
                    
                    <!-- Step 5: Meaningful Alt Text for Images -->
                    <img src="https://via.placeholder.com/600x300" alt="Clean HTML5 semantic code editor showing structural elements like header, main, and footer">
                    
                    <p>
                        Semantic HTML introduces elements that clearly describe their meaning to both the browser and the developer. 
                        By replacing generic <code>&lt;div&gt;</code> tags with structural tags like <code>&lt;header&gt;</code>, 
                        <code>&lt;main&gt;</code>, and <code>&lt;article&gt;</code>, web pages become significantly more accessible to screen readers 
                        and easier for search engines to index.
                    </p>
                </article>

                <!-- Article 2 -->
                <article>
                    <h3>Why Accessibility (a11y) Matters</h3>
                    <p class="meta">Published on <time datetime="2026-10-18">October 18, 2026</time> by <span>John Smith</span></p>
                    <p>
                        Web accessibility ensures that websites, tools, and technologies are designed and developed so that people with disabilities 
                        can use them easily. Incorporating screen-reader friendly markup, proper color contrast, keyboard navigation, and descriptive text alternative 
                        is critical for building an inclusive web.
                    </p>
                </article>
            </section>

        </main>

        <!-- Step 1: Sidebar content inside <aside> -->
        <aside aria-label="Sidebar Resources">
            <h3>Related Resources</h3>
            <!-- Step 6: Descriptive links -->
            <ul>
                <li><a href="https://developer.mozilla.org" target="_blank" rel="noopener">MDN Web Docs HTML Guide</a></li>
                <li><a href="https://www.w3.org/WAI/" target="_blank" rel="noopener">W3C Web Accessibility Initiative</a></li>
            </ul>
        </aside>
    </div>

    <!-- Step 1: Footer tag -->
    <footer>
        <p>&copy; 2026 Tech Insights. All rights reserved.</p>
    </footer>

</body>
</html>
Requirements Checklist Summary
Semantic Tags Used: <header>, <nav>, <main>, <section>, <article>, <aside>, and <footer>.

Navigation: Contained inside <nav> with unordered list structure (<ul>/<li>).

Main Content: Wrapped in <main>.

Heading Hierarchy: Logical structure followed (<h1> for site title, <h2> for major sections, <h3> for article sub-headings/sidebar titles).

Accessibility / Images: Added meaningful descriptive alt attribute (alt="Clean HTML5 semantic code editor showing structural elements like header, main, and footer").

Understandable Links: Replaced vague text with explicit anchor text and accessible focus outlines.

How to Complete Your Submission
Save the After Code as index.html (or your semantic HTML file).

Save the Before Code as before.html (optional, to render both side-by-side).

Open both HTML files in your browser and take two screenshots:

Screenshot 1: The before.html page rendered in your browser.

Screenshot 2: The updated index.html semantic page rendered in your browser.

Submit the index.html file and the before/after screenshots.