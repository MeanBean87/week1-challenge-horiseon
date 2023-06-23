# Week 1 Challenge Exercise - Horiseon Webpage

## Technology Used

| Technology Used |                                            Resource URL                                            |
| --------------- | :-------------------------------------------------------------------------------------------------: |
| HTML            | [https://developer.mozilla.org/en-US/docs/Web/HTML](https://developer.mozilla.org/en-US/docs/Web/HTML) |
| CSS             |  [https://developer.mozilla.org/en-US/docs/Web/CSS](https://developer.mozilla.org/en-US/docs/Web/CSS)  |
| Git             |                              [https://git-scm.com/](https://git-scm.com/)                              |

## Description

[Visit the Deployed Site](https://meanbean87.github.io/week1-challenge-horiseon/)

This is not an actual company.

This is a homework challenge that required the student to update code to satisify the below user story:

User Story

```plaintext
AS A marketing agency
I WANT a codebase that follows accessibility standards
SO THAT our own site is optimized for search engines
```

Acceptance Criteria

```plaintext
GIVEN a webpage meets accessibility standards
WHEN I view the source code
THEN I find semantic HTML elements
WHEN I view the structure of the HTML elements
THEN I find that the elements follow a logical structure independent of styling and positioning
WHEN I view the icon and image elements
THEN I find accessible alt attributes
WHEN I view the heading attributes
THEN they fall in sequential order
WHEN I view the title element
THEN I find a concise, descriptive title
```

The source code did not follow proper HTML semantics, many overly used div containers and improper use of HTML tags as well as a broken link. The images did not provide accessibility for screen readers. The CSS file contained many redundant declarations that caused significant code bloat and sections needed to be commented to provide better readability. This required code refactoring for both HTML and CSS elements.

## Site Demo

![Site Langing Page](./assets/images/site.gif)

## Table of Contents

If your README is very long, add a table of contents to make it easy for users to find what they need.

* [Code Refactor Example](#code-refactor-example)
* [Usage](#usage)
* [Learning Points](#learning-points)
* [Author Info](#author-info)
* [Credits](#credits)
* [License](#license)

## Code Refactor Example

What are the steps required to install your project? Provide a step-by-step description of how to get the development environment running.

```html
<div class="header">
        <h1>Hori<span class="seo">seo</span>n</h1>
        <div>
            <ul>
                <li>
                    <a href="#search-engine-optimization">Search Engine Optimization</a>
                </li>
                <li>
                    <a href="#online-reputation-management">Online Reputation Management</a>
                </li>
                <li>
                    <a href="#social-media-marketing">Social Media Marketing</a>
                </li>
            </ul>
        </div>
    </div>
```

Converting the above non-semantic div with the class of 'header' to an appropriate [`<header>` semantic element](https://www.w3schools.com/html/html5_semantic_elements.asp).

```html
<header>
        <h1>Hori<span class="seo">seo</span>n</h1>
        <nav>
            <ul>
                <li>
                    <a href="#search-engine-optimization">Search Engine Optimization</a>
                </li>
                <li>
                    <a href="#online-reputation-management">Online Reputation Management</a>
                </li>
                <li>
                    <a href="#social-media-marketing">Social Media Marketing</a>
                </li>
            </ul>
        </nav>
    </header>

```

This change require some additional modification to the CSS selector:

```css
.header {
    padding: 20px;
    font-family: 'Trebuchet MS', 'Lucida Sans Unicode', 'Lucida Grande', 'Lucida Sans', Arial, sans-serif;
    background-color: #2a607c;
    color: #ffffff;
}
```

No longer targeting the element on the page with the class of 'header' but instead the css selector targeting the 'header' element

```css
header {
    padding: 20px;
    font-family: 'Trebuchet MS', 'Lucida Sans Unicode', 'Lucida Grande', 'Lucida Sans', Arial, sans-serif;
    background-color: #2a607c;
    color: #ffffff;
}

```

## Usage

1. Clone repository to your selected directory.
2. Open with source code editor or IDE of your choice.
3. Edit source code and deploy to web hosting provider if desired.

## Learning Points

This project afforded a valuable opportunity to explore and comprehend the distinctions between semantic HTML elements and their non-semantic counterparts. Additionally, it served as a beneficial platform for honing skills in minimizing superfluous CSS properties.

## Author Info

#### Michael Mattingly

* [LinkedIn](https://www.linkedin.com/in/michael-mattingly-5580b1280/)
* [Github](https://github.com/MeanBean87)

## Credits

 The Complete Web Development Bootcamp 2023 - Angela Yu.

* [Udemy](https://www.udemy.com/course/the-complete-web-development-bootcamp/)

## License

The content of this project is licensed under the [MIT License](https://opensource.org/licenses/MIT).
