Soul Cycle Shop 
======
<br>

## General Functionality
[Fix] When navigating to Soul Shop via a specific product link, the user is redirected to the homepage instead of the specified product pages
* [Expected-Behavior] When navigating to the Soul Shop via a specific product page, the site should direct me to the specified product page

[Change] Re-enabled focus outline to ensure site accessibility
* Existing style sheet removes the focus outline; this is neccessary to ensure users using some types of accessible technologies (or with some accessibility needs) are able to navigate and use the site
* [Solution] Re-enable the focus outline by elimniating this line from all stylesheets
    ```css
    outline: none;
    ```
    * Implement an alternative that enables the outline for keyboard users, but removes it for mouse users [[link]](https://medium.com/better-programming/a11y-never-remove-the-outlines-ee4efc7a9968)
    * In addtion, perform a more throughout audit of the styling and usability of tab based navigation on the site; making necessary changes based off results

<br>

## Shop Home
`tbd`

<br>

## Search Results
`tbd`

<br>

## Product Pages

[Change] Change symbols in breadcrumbs to make it easier to identify them as breadcrumbs
* Currently there is a ‘-’ between each breadcrumb item
* [Solution] Change '-' to '>'
    ```css
    .c-breadcrumbs__item:not(:last-child)::after {
    content: '>';
    display: inline-block;
    position: absolute;
    left: 100%;
    top: 0;
    width: 0.75rem;
    text-align: center; }
    ```
<br>

[Change] Change styling of linked text to make it clear that items are selectable
* The majority of clickable text has no indication that it is clickable, other than the 
curser change on hover
* [Solution] Underline text upon hover




