# nutritionLabel
Free Code Camp - Learn typography by building a nutrition label.

## **Step 1** 
We've provided a basic HTML boilerplate for you.<br>
Create an `h1` element within your `body` element and give it the text `Nutrition Facts`.

```html
<h1>Nutrition Facts</h1>
```

## **Step 2** 
Below your `h1` element, add a `p` element with the text `8 servings per container`.

```html
<p>8 servings per container</p>
```

## **Step 3** 
Add a second `p` element with the text `Serving size 2/3 cup (55g)`.

```html
<p>Serving size 2/3 cup (55g)</p>
```

## **Step 4** 
Within your `head` element, add a `link` element with the `rel` attribute set to `stylesheet` and the `href` attribute set to `https://fonts.googleapis.com/css?family=Open+Sans:400,700,800`.<br>
This will import the `Open Sans` font family, with the font weight values `400`, `700`, and `800`.<br>
Also add a `link` element to link your `styles.css` file.

```html
<link rel="stylesheet" href="https://fonts.googleapis.com/css?family=Open+Sans:400,700,800">
<link rel="stylesheet" href="styles.css">
```

## **Step 5** 
Create a `body` selector and give it a `font-family` set to `Open Sans` with a fallback of `sans-serif`.<br>
Remember that fonts with spaces in the name must be wrapped in quotes for CSS.

```css
body {
  font-family: "Open Sans", sans-serif
}
```

## **Step 6** 
The font is a bit small. Create an `html` selector and set the font to have a size of `16px`.

```css
body {
  font-family: "Open Sans", sans-serif
}
```

## **Step 7** 
Wrap your `h1` and `p` elements in a `div` element. Give that `div` a `class` attribute set to `label`.

```html
<div class="label">
    <h1>Nutrition Facts</h1>
    <p>8 servings per container</p>
    <p>Serving size 2/3 cup (55g)</p>
</div>
```

## **Step 8** 
Borders can be used to group and prioritize content.<br>
Create a `.label` selector and give it a `border` set to `2px solid black`.

```css
.label {
  border: 2px solid black;
}
```

## **Step 9** 
Good use of white space can bring focus to the important elements of your page, and help guide your user's eyes through your text.<br>
Give your `.label` selector a `width` property set to `270px`.

```css
width: 270px;
```

## **Step 10** 
Give your `.label` selector a `margin` property set to `20px auto`, and a `padding` property set to `0 7px`.

```css
margin: 20px auto;
padding: 0 7px;
```

## **Step 11** 
If you inspect your `.label` element with your browser's developer tools, you may notice that it's actually 288 pixels wide instead of 270. This is because, by default, the browser includes the border and padding when determining an element's size.<br>
To solve this, reset the box model by creating a `*` selector and giving it a `box-sizing` property of `border-box`.

```css
* {
  box-sizing: border-box
}
```

## **Step 12** 
Remember that the use of `h1`, `h2`, and similar tags determine the semantic structure of your HTML. However, you can adjust the CSS of these elements to control the visual flow and hierarchy.<br>
Create an `h1` rule and set the `font-weight` property to `800`. This will make your `h1` text bolder.

```css
h1 {
  font-weight: 800;
}
```

## **Step 13** 
Give your `h1` selector a `text-align` property of `center`.

```css
text-align: center;
```

## **Step 14** 
Fine-tune the placement of your `h1` by giving it a top and bottom margin of `-4px` and a left and right margin of `0`.

```css
margin: -4px 0;
```

## **Step 15** 
Create a `p` selector and remove all margins.

```css
p {
  margin: 0;
}
```

## **Step 16** 
Give your `.label` selector a `margin` property set to `20px auto`, and a `padding` property set to `0 7px`.

```html
<div class="divider"></div>
```

## **Step 17** 
Create a selector for your new `.divider` and set the `border-bottom` property to `1px solid #888989`. Also give it a top and bottom margin of `2px`. It should not have any left or right margin.

```css
.divider {
  border-bottom: 1px solid #888989;
  margin: 2px 0;
}
```

## **Step 18** 
The `letter-spacing` property can be used to adjust the space between each character of text in an element.<br>
Give your `h1` selector a `letter-spacing` property set to `0.15px` to space them out a bit more.

```css
letter-spacing: 0.15px;
```

## **Step 19** 
Nutrition labels have a lot of bold text to draw attention to important information. Rather than targeting each element that needs to be bold, it is more efficient to use a class to apply the bold styling to every element.<br>
Give your second `p` element a `class` attribute set to `bold`.

```html
<p class="bold">Serving size 2/3 cup (55g)</p>
```

## **Step 20** 
Your new class does not have any styling yet. Create a `.bold` selector and give it a `font-weight` property set to `800` to make the text bold.<br>
Go ahead and remove the `font-weight` property from your `h1` selector as well.

```css
.bold {
  font-weight:800
}
```

## **Step 21** 
Give your `h1` element a `class` attribute set to `bold`. This will make the text bold again.

```html
<h1 class="bold">Nutrition Facts</h1>
```

## **Step 22** 
Horizontal spacing between equally important elements can increase the readability of your text.<br>
Wrap the text `2/3 cup (55g)` in a `span` element.

```html
<p class="bold">Serving size <span>2/3 cup (55g)</span></p>
```

## **Step 23** 
Now we can add the horizontal spacing using `flex`. In your `p` selector, add a `display` property set to `flex` and a `justify-content` property set to `space-between`.

```css
display: flex;
justify-content: space-between;
```

## **Step 24** 
Wrap everything within the `.label` element in a new `header` element.

```html
<div class="label">
  <header>
    <h1 class="bold">Nutrition Facts</h1>
    <div class="divider"></div>
    <p>8 servings per container</p>
    <p class="bold">Serving size <span>2/3 cup (55g)</span></p>
  </header>
</div>
```

## **Step 25** 
Now update your `h1` selector to be `header h1` to specifically target your `h1` element within your new `header`.

```css
header h1 {
  text-align: center;
  margin: -4px 0;
  letter-spacing: 0.15px
}
```

## **Step 26** 
Create a new `div` element below your `header` element, and give it a `class` attribute set to `divider large`.

```html
<div class="divider large"></div>
```

## **Step 27** 
Create a new `.large` selector and give it a `height` property set to `10px`. Also create an `.large, .medium` selector and set the `background-color` property to `black`.

```css
.large {
  height: 10px;
}

.large, .medium {
  background-color: black;
}
```

## **Step 28** 
You may notice there is still a small border at the bottom of your `.large` element. To reset this, give your `.large, .medium` selector a `border` property set to `0`.<br>
Note: the `medium`(medium) class will be utilized later for the thinner bars of the nutrition label.

```css
border: 0;
```

## **Step 29** 
Create a new `div` below your `.large` element and give it a `class` attribute set to `calories-info`.

```html
<div class="calories-info"></div>
```

## **Step 30** 
Within your `.calories-info element, create a `div element. Give that `div` element a `class` attribute set to `left-container`. Within the newly created `div` element, create a `h2` element with the text `Amount per serving`. Give the `h2` element a `class` attribute set to `bold small-text`.

```html
<div class="left-container">
  <h2 class="bold small-text">Amount per serving</h2>
</div>
```

## **Step 31** 
The `rem` unit stands for `root em`, and is relative to the font size of the `html` element.<br>
Create a `.small-text` selector and set the `font-size` to `0.85rem`, which would calculate to roughly `13.6px` (remember that you set your `html` to have a `font-size` of `16px`).

```css
.small-text {
  font-size: 0.85rem
}
```

## **Step 32** 
Create a `.calories-info h2` selector and remove all margins.

```css
.calories-info h2
```

## **Step 33** 
Below your `.small-text` element, create a new `p` element with the text `Calories`. Also below the `.left-container` element, create a new `span` element with the text `230`.

```html
<div class="left-container">
  <h2 class="bold small-text">Amount per serving</h2>
  <p>Calories</p>
</div>
<span>230</span>
```

## **Step 34** 
Create a new `.calories-info` selector and give it a `display` property set to `flex`. Also give it a `justify-content` property set to `space-between` and `align-items` property set to `flex-end`.

```css
.calories-info {
  display: flex;
  justify-content: space-between;
  align-items: flex-end;
}
```

## **Step 35** 
Create a new `.left-container p` selector setting the top and bottom margin to `-5px`, and the left and right margin to `-2px`. Also set the `font-size` to `2em` and `font-weight` to `700`.

```css
.left-container p {
  margin: -5px -2px;
  font-size: 2em;
  font-weight: 700;
}
```

## **Step 36** 
Create a `.calories-info span` selector, set its `font-size` to `2.4em` and `font-weight` to `700`.

```css
.calories-info span {
  font-size: 2.4em;
  font-weight: 700;
}
```

## **Step 37** 
Typography is often more art than science. You may have to tweak things like alignment until it looks correct.<br>
Give your `.calories-info` span selector a `margin` set to `-7px -2px`. This will shift your `230` text into place.

```css
margin: -7px -2px;
```

## **Step 38** 
Below your `.calories-info` element, add a `div` with the `class` attribute set to `divider medium`.

```html
<div class="divider medium"></div>
```

## **Step 39** 
Create an `.medium` selector and give it a `height` property of `5px`.

```css
.medium {
  height: 5px;
}
```

## **Step 40** 
Create a new `div` element below your `.medium` element. Give it a `class` attribute set to `daily-value small-text`. Within this new `div`, add a `p` element with the text `% Daily Value *`, and set the `class` attribute to `bold right`.

```html
<div class="divider medium"></div>
<div class="daily-value small-text">
  <p class="bold right">% Daily Value *</p>
</div>
```

## **Step 41** 
The text `% Daily Value *` should be aligned to the right. Create a `.right` selector and use the `justify-content` property to do it.

```css
.right {
  justify-content: flex-end;
}
```

## **Step 42** 
Use your existing `.divider` element as an example to add a new divider after the `p` element.

```html
<div class="divider"></div>
```

## **Step 43** 
After your last `.divider` element, create a `p` element and give it the text `Total Fat 8g 10%`. Wrap the text `Total Fat` in a `span` element with the `class` of `bold`. Wrap the text `10%` in another `span` element with the `class` of `bold`. Finally, nest the `Total Fat` `span` element and the text `8g` in an additional `span` element for alignment.

```html
<p><span><span class="bold">Total Fat</span>8g</span><span class="bold">10%</span></p>
```

## **Step 44** 
Below your element with the `Total Fat` text, create a new `p` element with the text `Saturated Fat 1g 5%`. Wrap the `5%` in a `span` with the `class` attribute set to `bold`. In this case this is enough to align the percentage to `5%`.

```html
<p>Saturated Fat 1g <span class="bold">5%</span></p>
```

## **Step 45** 
This new `p` element will need to be indented. Give it a `class` set to `indent`

```html
<p class="indent">Saturated Fat 1g <span class="bold">5%</span></p>
```

## **Step 46** 
Create a new `.indent` selector and give it a `margin-left` property set to `1em`.

```css
.indent {
  margin-left: 1em;
}
```

## **Step 47** 
Create a `.daily-value p` selector to target all of your `p` elements in the `daily-value` section. Give this new selector a `border-bottom` set to `1px solid #888989`.

```css
.daily-value p {
  border-bottom: 1px solid #888989;
}
```

## **Step 48** 
The bottom borders under your `% Daily Value *` and `Saturated Fat 1g 5%` elements do not extend the full width of the label. Add `no-divider` to the `class` for these two elements.

```html
<p class="bold right no-divider">% Daily Value *</p>
<p class="indent no-divider">Saturated Fat 1g <span class="bold">5%</span></p>
```

## **Step 49** 
The `:not` pseudo-selector can be used to select all elements that do not match the given CSS rule.<br>
`div:not(#example) {` <br>
  `color: red;`<br>
`}`<br
The above selects all `div` elements without an `id` of `example`.<br>
Modify your `.daily-value p` selector to exclude the `.no-divider` elements.

```css
.daily-value p:not(.no-divider) {
  border-bottom: 1px solid #888989;
}
```

## **Step 50** 
Now you will have to add separate dividers below your `.no-divider elements`.<br>
Your first `.no-divider` element has a `.divider` after it. Create another `.divider` after your second `.no-divider` element.

```html
<div class="divider"></div>
```

## **Step 51** 
After your last `.divider`, create another `p` element with the text `Trans Fat 0g`. Italicize the word `Trans` by wrapping it in an `i` element. Give the new `p` element the `class` attribute set to `indent no-divider`. Wrap `Trans Fat 0g` in a `span` element for alignment.

```html
<p class="indent no-divider"><span><i>Trans</i> Fat 0g</span></p>
```

## **Step 52** 
Create another `.divider` after your last `p` element.

```html
```

## **Step 53** 
After your last `.divider`, create a new `p` element with the text `Cholesterol 0mg 0%`. Wrap the text `Cholesterol` in a `span` element, and give that `span` element the `class` of `bold`. Wrap the text `0%` in another `span` element, with the `class` of `bold`. Finally, nest the `Cholesterol` `span` element and the text `0mg` in an additional `span` element for alignment.

```html
<p><span><span class="bold">Cholesterol</span>0mg</span><span class="bold">0%</span></p>
```

## **Step 54** 
Below your last `p` element, create another `p` element with the text `Sodium 160mg 7%`. Wrap the text `Sodium` in a `span` element with a `class` attribute set to `bold`. Wrap the `7%` text in another `span` element with the `class` set to `bold`. Also add an additional `span` element around `Sodium 160mg` for aligning it correctly.

```html
<p><span><span class="bold">Sodium</span>160mg</span> <span class="bold">7%</span></p>
```

## **Step 55** 
Below your last `p` element, add another `p` element with the text `Total Carbohydrate 37g 13%`. Like before, use `span` elements to make the text `Total Carbohydrate` and `13%` bold. Also add an additional `span` element around the `Total Carbohydrate 37g` text to have it aligned to the left and `13%` to the right.

```html
<p><span><span class="bold">Total Carbohydrate</span> 37g</span><span class="bold">13%</span></p>
```

## **Step 56** 
Below your last `p` element, add another `p` element with the text `Dietary Fiber 4g`. Give the `p` element the `class` necessary to indent it and remove the dividing border. Then create a divider below that `p` element.

```html
<p class="indent no-divider"><span><span class="bold">Dietary Fiber</span> 4g</p>
<div class="divider"></div>
```

## **Step 57** 
Create another `p` element after your last `.divider`, and give it the text `Total Sugars 12g`. Assign that `p` element the `class` values necessary to indent it and remove the bottom border. Then create another `.divider` below your new `p` element.

```html
<p class="indent no-divider">Total Sugars 12g</p>
<div class="divider"></div>
```

## **Step 58** 
The advantage to creating these dividers is that you can apply specific classes to style them individually. Add `double-indent` to the `class` for your last `.divider`.

```html
<div class="double-indent divider"></div>
```

## **Step 59** 
Create a `.double-indent` selector and give it a left margin of `2em`.

```css
.double-indent {
  margin-left: 2em;
}
```

## **Step 60** 
Below your `.double-indent` element, add a new `p` element with the text `Includes 10g Added Sugars 20%`. Your new `p` element should also be double indented, and have no bottom border. Use a `span` to make the `20%` bold and right aligned.<br>
Then create another divider after that `p` element.

```html
<p class="double-indent no-divider">Includes 10g Added Sugars<span class="bold">20%</span></p>
<div class="divider"></div>
```

## **Step 61** 
After your last divider, create another `p` element with the text `Protein 3g`. Use the necessary classes to remove the bottom border, and a `span` to make the `Protein` bold.<br>
Following this element, create a large divider.

```html
<p class="no-divider"><span class="bold">Protein</span>3g</p>
<div class="divider large"></div>
```

## **Step 62** 
Create another `p` element below your large divider. Give the `p` element the text `Vitamin D 2mcg 10%`.<br>
The `p` element contains only text, you can wrap the percentage in a `span` element so that it is considered a separate entity from the rest of the text, and it's moved to the right.

```html
<p>Vitamin D 2mcg<span>10%</span></p>
```

## **Step 63** 
Create another `p` element, give it the text `Calcium 260mg 20%`. Align `20%` to the right. Below that, create a `p` element with the text `Iron 8mg 45%`, aligning the `45%` to the right.

```html
<p>Calcium 260mg<span>20%</span></p>
<p>Iron 8mg<span>45%</span></p>
```

## **Step 64** 
Create the final `p` element for your `.daily-value` section. Give it the text `Potassium 235mg 6%`. Align the `6%` text to the right, and remove the bottom border of the `p` element.

```html
<p class="no-divider">Potassium 235mg <span>6%</span></p>
```

## **Step 65** 
Add a medium divider after your `.daily-value` element. Below that new divider, create a `p` element with the `class` attribute set to `note`.<br>
Give the `p` element the following text:<br>
`* The % Daily Value (DV) tells you how much a nutrient in a serving of food contributes to a daily diet. 2,000 calories a day is used for general nutrition advice.`

```html
<div class="medium divider"></div>
<p class="note">* The % Daily Value (DV) tells you how much a nutrient in a serving of food contributes to a daily diet. 2,000 calories a day is used for general nutrition advice.</p>
```

## **Step 66** 
Create a `.note` selector, and set the size of the font to `0.6rem`. Also set the top and bottom margins to `5px`, removing the left and right margins.

```css
.note {
  font-size: 0.6rem;
  margin: 5px 0;
}
```

## **Step 67** 
Give the `.note` selector a left and right padding of `8px`, removing the top and bottom padding. Also set the `text-indent` property to `-8px`.<br>
With these last changes, your nutrition label is complete!

```css
padding: 0 8px;
text-indent: -8px;
```