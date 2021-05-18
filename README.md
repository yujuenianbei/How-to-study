# Accessibility

## Homepage/CMS 

https://store.hp.com/sg-en/default

### ARIA (1 day)

- [aria-hidden="true"] elements contain focusable descendents

  we should use

  ```
  content[aria-hidden=true] {
    display:none;
  }
  ```

- [role]s do not have all required [aria-*] attributes
  
  input#search.input-text need add more aria-* attributes to show user what they search for

- [role]s are not contained by their required parent element

  THe 'support' in top menu do no not have ``` role="presentation" ``` attributes

### Contrast (2 days)

- Background and foreground colors do not have a sufficient contrast ratio.

  This need design team give us a better solution.

- [id] attributes on active, focusable elements are not unique

  In menu the element id like ```ui-id-*``` is not unique

  doc: <a href="https://web.dev/duplicate-id-active/">duplicate-id-active</a>

- Heading elements are not in a sequentially-descending order

  This need design team give us a better solution.

  such as this:

  ```
    <div class="contents">
      <h3 class="darkblue"><span class="white">HP Print Rewards</span></h3>
      <div class="clear_10h"></div>
      <h1 class="white">FREE* eCapita Vouchers<br class="hide_for_md">worth up to $80</h1>
      <h4 class="white">with selected Print purchases</h4>
    </div>
  ```
  In this sample we escape to use ```<h2></h2>``` element.

  doc: <a href="https://web.dev/heading-order/">heading-order</a>

### Names and labels

- Links do not have a discernible name

  In SEO we had added the title attribute to all link except the code which can be edit in backend

### Tables and lists (2 days)

- List items (```<li>```) are not contained within ```<ul>``` or ```<ol>``` parent elements.
  
  ```
  <li class="level0 level-top ui-menu-item">
    ...
  </li>
  ```
  This ```<li>``` element has added in ```<ul>``` but we have two javascript code has added before this element.

### Best practices

- [user-scalable="no"] is used in the <meta name="viewport"> element or the [maximum-scale] attribute is less than 5.

  I suggest we should not use this suggestion because if we use the suggestion uer can scale our website and scroll left or right. We need some suggestions from Desgin Team.

## PLP 

https://store.hp.com/sg-en/default/laptops-tablets.html

(ignore the same suggestions )

### ARIA (2 days)

- [aria-*] attributes are not valid or misspelled

  ```
  <div class="data item title title-view-all active" ... >

  </div>
  ```

- ARIA IDs are not unique
  
  The toolbar of product list has added on both head and footer and the head part has been hide if we remove head part the sort will be effected.

### Names and labels (2 days)

- Form elements do not have associated labels

  Filter input element has not add associated label to make sure how this input will effect the search result. We should add label for this input element.

## PDP 

https://store.hp.com/sg-en/default/laptops-tablets/hp-laptop-15s-fq2024tu-2p1q1pa.html

### Names and labels (1 day)

- Image elements do not have [alt] attributes

  We will fix this part of recommendations-products images within 1 day

- Links do not have a discernible name

  We will fix this part of recommendations-products images url description within 1 day

### Navigation (2 day)

- Heading elements are not in a sequentially-descending order
  
  Overview of product should change ```<h4>``` element. We need some time to check all products to fix this suggestion


So we need more than 12 workday to improve our Accessibility score
