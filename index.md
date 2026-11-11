Assignment 5.3 — Typography Showcase Page
Here is your complete, professional typography showcase page. It pairs two complementary Google Fonts (Poppins for clean, striking headings and Inter for readable body text), customizes font weights, sizes, spacing, and styling, and is organized precisely into the three required sections.

1. The External Stylesheet (style.css)
Save this file as style.css. It implements all typography rules, custom Google Fonts, spacing adjustments, and text decorations.

CSS
/* --- Google Fonts Import --- */
@import url('https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500;600&family=Poppins:wght@500;600;700;800&display=swap');

/* --- Reset & Global Body Styles (Steps 1, 2, & 3) --- */
* {
    box-sizing: border-box;
    margin: 0;
    padding: 0;
}

body {
    font-family: 'Inter', sans-serif; /* Body font family */
    background-color: #f7f9fc;
    color: #2d3748;
    line-height: 1.7; /* Step 5: Adjusted line-height */
    padding: 2.5rem 1rem;
}

/* --- Main Container --- */
.container {
    max-width: 850px;
    margin: 0 auto;
    background: #ffffff;
    padding: 3rem;
    border-radius: 12px;
    box-shadow: 0 4px 15px rgba(0, 0, 0, 0.05);
}

/* --- Global Headings (Step 2: Heading Font Family) --- */
h1, h2, h3, h4 {
    font-family: 'Poppins', sans-serif; 
    color: #1a202c;
}

/* Main Page Header */
header {
    text-align: center;
    margin-bottom: 2.5rem;
    border-bottom: 2px solid #e2e8f0;
    padding-bottom: 1.5rem;
}

header h1 {
    font-size: 2.75rem;
    font-weight: 800;
    letter-spacing: -0.02em; /* Step 5: Letter-spacing */
    margin-bottom: 0.5rem;
    color: #2b6cb0;
}

header p {
    font-size: 1.1rem;
    color: #718096;
    font-weight: 300;
}

/* Section Styling */
section {
    margin-bottom: 2.5rem;
}

section h2 {
    font-size: 1.6rem;
    font-weight: 700;
    margin-bottom: 1rem;
    padding-bottom: 0.3rem;
    border-bottom: 2px solid #cbd5e0;
}

/* --- Section 1: Heading Styles --- */
.heading-box h3 {
    font-size: 1.35rem;
    font-weight: 600;
    margin-top: 1rem;
    color: #319795;
}

.heading-box h4 {
    font-size: 1.1rem;
    font-weight: 500;
    margin-top: 0.5rem;
    color: #4a5568;
    letter-spacing: 0.05em; /* Step 5 */
}

/* --- Section 2: Paragraph Styles --- */
p {
    margin-bottom: 1rem;
    font-size: 1rem;
    font-weight: 400;
}

.lead-paragraph {
    font-size: 1.15rem;
    font-weight: 500;
    color: #2d3748;
    line-height: 1.8;
}

.justified-paragraph {
    text-align: justify; /* Step 4: text-align */
    color: #4a5568;
}

.tracked-paragraph {
    letter-spacing: 0.08em; /* Step 5: wider letter spacing */
    color: #4a5568;
}

/* --- Section 3: Text Emphasis --- */
.italic-text {
    font-style: italic; /* Step 4: font-style */
    color: #dd6b20;
}

.bold-text {
    font-weight: 600; /* Step 3: font weight */
    color: #805ad5;
}

.underline-text {
    text-decoration: underline; /* Step 4: text-decoration */
    text-decoration-color: #3182ce;
    text-underline-offset: 4px;
}

.strikethrough-text {
    text-decoration: line-through; /* Step 4: text-decoration */
    color: #a0aec0;
}

/* Footer */
footer {
    text-align: center;
    margin-top: 3rem;
    font-size: 0.85rem;
    color: #a0aec0;
    border-top: 1px solid #edf2f7;
    padding-top: 1.5rem;
}
2. The HTML File (index.html)
Save this file as index.html. It incorporates Google Fonts, links to style.css, and builds the three required sections.

HTML
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Typography Showcase</title>
    
    <!-- Google Fonts Links -->
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500;600&family=Poppins:wght@500;600;700;800&display=swap" rel="stylesheet">
    
    <!-- External Stylesheet -->
    <link rel="stylesheet" href="style.css">
</head>
<body>

    <div class="container">
        
        <!-- Page Header -->
        <header>
            <h1>Typography Showcase</h1>
            <p>An exploration of web typography using Google Fonts, weights, sizes, and spacing properties.</p>
        </header>

        <main>
            <!-- SECTION 1: Heading Styles -->
            <section class="heading-box">
                <h2>1. Heading Styles</h2>
                <p>Headings use the <strong>Poppins</strong> font family with various weights, sizes, and custom letter-spacing.</p>
                
                <h1>Heading 1 (Poppins 800 - Extra Bold)</h1>
                <h2>Heading 2 (Poppins 700 - Bold)</h2>
                <h3>Heading 3 (Poppins 600 - Semi-Bold)</h3>
                <h4>Heading 4 (Poppins 500 - Medium with Wide Tracking)</h4>
            </section>

            <!-- SECTION 2: Paragraph Styles -->
            <section>
                <h2>2. Paragraph Styles</h2>
                <p>Paragraphs use the <strong>Inter</strong> font family with adjusted line heights, font sizes, and alignment.</p>
                
                <p class="lead-paragraph">This is a lead paragraph. It uses a slightly larger font size (1.15rem), medium weight, and a relaxed line-height of 1.8 to draw the reader's attention right away.</p>
                
                <p class="justified-paragraph">This is a standard body paragraph set with text-align: justify. Proper justification helps create clean, block-like margins on both sides of the content column, which is common in editorial design and article layouts.</p>
                
                <p class="tracked-paragraph">This paragraph demonstrates custom letter-spacing (tracking). Spacing out letters slightly can add a clean, modern touch to short introductory snippets or callout descriptions.</p>
            </section>

            <!-- SECTION 3: Text Emphasis -->
            <section>
                <h2>3. Text Emphasis</h2>
                <p>This section showcases font styles, text decorations, and distinct font weights to highlight specific words or phrases.</p>
                
                <p><span class="italic-text">Italicized text</span> is used for emphasis, foreign words, titles of works, or internal thoughts.</p>
                
                <p><span class="bold-text">Semi-bold text weight</span> helps draw the eye to key vocabulary or important technical terms within a sentence.</p>
                
                <p><span class="underline-text">Underlined text</span> can draw attention to hyperlinks or highlighted data points.</p>
                
                <p><span class="strikethrough-text">Strikethrough text</span> is helpful for showing outdated pricing, completed task lists, or corrections.</p>
            </section>
        </main>

        <footer>
            <p>&copy; 2026 Typography Showcase Assignment. All fonts provided by Google Fonts.</p>
        </footer>

    </div>

</body>
</html>
Step Summary Checklist:
Complementary Fonts (Step 1 & 2): Linked Poppins for headings and Inter for body text via Google Fonts.

Font Sizes & Weights (Step 3): Applied various weights (300, 400, 500, 600, 700, 800) across titles and text.

Text Properties (Step 4): Applied text-align: justify;, font-style: italic;, and text-decoration: underline / line-through;.

Spacing Adjustments (Step 5): Tuned body line-height to 1.7 and customized letter-spacing (tracking) on headings and lead paragraphs.

Required Sections (Step 6): Structured the page cleanly into Heading Styles, Paragraph Styles, and Text Emphasis.

Want me to help you style code blocks or blockquotes for your next typography or blogging assignment?

Yes