# CSS Grid Testimonial Project  

This project was an opportunity to practice **CSS Grid** to create a structured and responsive testimonial layout. Below, I’ve documented key concepts I learned while working on this project.  

---

## What I Learned About CSS Grid  

### 1. Grid Template Columns  

The `grid-template-columns` property defines how many columns a grid should have and their sizes.  

```css
.testimonial-grid {
    display: grid;
    grid-template-columns: repeat(4, 1fr);
    gap: 20px;
}
This means the grid will have 4 equal columns, and each column will take up an equal portion of the available space.

2. Grid Template Rows
The grid-template-rows property defines the height of each row. Since content height varies, I used auto to allow the rows to expand dynamically.
```css
.testimonial-grid {
    grid-template-rows: auto auto;
}

3. Spanning Across Columns and Rows
Some testimonial cards needed to span multiple columns or rows. I achieved this using grid-column and grid-row.

To make an element span two columns, I used:

```css
.purple {
    grid-column: span 2;
}

**To make a card span two rows, I could use:**

```css
.kira {
    grid-row: span 2;
}

4. Using Grid Template Areas
Instead of placing elements manually using row and column numbers, I used grid-template-areas to make the layout more readable.

```css
.testimonial-grid {
    grid-template-areas: 
        "purple purple blue kira"
        "white dark dark kira";
}
**Then, I assigned each testimonial card to a specific area:**

```css
.purple { grid-area: purple; }
.kira { grid-area: kira; }


**5. Making the Grid Responsive**
To ensure the layout looks good on different screen sizes, I used media queries.

For tablet screens, I reduced the number of columns:

```css
@media (max-width: 1024px) {
    .testimonial-grid {
        grid-template-columns: repeat(2, 1fr);
    }
}

**For mobile screens, I switched to a single-column layout:
**

```css
@media (max-width: 375px) {
    .testimonial-grid {
        grid-template-columns: 1fr;
    }
}

Author
👤 [Ukpong-Inyang]

GitHub: https://github.com/queenieukpong/

LinkedIn: https://www.linkedin.com/in/inyang


**This project helped me understand CSS Grid, including grid-template properties, spanning elements, and responsive design. Now, I feel more confident in structuring layouts using CSS Grid!**

```css




## My process

### Built with

- Semantic HTML5 markup
- CSS custom properties
- Flexbox
- CSS Grid


### What i learned


To see how you can add code snippets, see below:

```html
<div class="testimonial-container">
        <div class="testimonial-grid">
```

```css
.testimonial-grid {
    display: grid;
    grid-template-columns: repeat(4, 1fr);
    grid-template-rows: auto auto;
    gap: 20px;
    grid-template-areas: 
        "purple purple blue kira"
        "white dark dark kira";
}
```


### Continued development

Below is an Image of Progress this far
![Testimonial Grid Screenshot](/images/css-testimonial-grid.png)


### Useful resources

- [w3Schools](https://www.w3schools.com/css/) - This helped me for when i needed more clarity on css Grid column. I really liked this pattern and will use it going forward.
- [Heros World](https://www.herosworld.org) - This is an amazing article which helped me finally understand CSS Grid. I'd recommend it to anyone still learning fullstack and needs to grab important concepts in front end HTML and CSS.
