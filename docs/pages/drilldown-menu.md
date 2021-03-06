---
title: Drilldown Menu
description: Drilldown is one of Foundation's three menu patterns, which converts a series of nested lists into a vertical drilldown menu.
scss: scss/components/_drilldown.scss
js: js/foundation.drilldown.js
---

## Basics

Drilldowns use the standard [Menu](menu.html#nested-style) syntax, using `<ul>`, `<li>`, and `<a>`. Add `data-drilldown` to the root menu to set up the drilldown.

To create sub-menus, place a `<ul>` *next to* an `<a>`. Clicking that `<a>` will then open the `<ul>` that it's next to.

Any `<a>` without a submenu will function like a normal link.

```html
<ul class="vertical menu" data-drilldown>
  <li>
    <a href="#Item-1">Item 1</a>
    <ul class="vertical menu">
      <li><a href="#Item-1A">Item 1A</a></li>
      <!-- ... -->
    </ul>
  </li>
  <li><a href="#Item-2">Item 2</a></li>
</ul>
```

<div class="primary callout">
  <p>The drilldown menu takes on the height of the tallest menu in the hierarchy, so the menu doesn't change height as the user navigates it.</p>
</div>

<ul class="menu" data-drilldown style="width: 200px" id="m1">
  <li>
    <a href="#">Item 1</a>
    <ul class="menu">
      <li>
        <a href="#">Item 1A</a>
        <ul class="menu">
          <li><a href="#Item-1Aa">Item 1Aa</a></li>
          <li><a href="#Item-1Ba">Item 1Ba</a></li>
          <li><a href="#Item-1Ca">Item 1Ca</a></li>
          <li><a href="#Item-1Da">Item 1Da</a></li>
          <li><a href="#Item-1Ea">Item 1Ea</a></li>
        </ul>
      </li>
      <li><a href="#Item-1B">Item 1B</a></li>
      <li><a href="#Item-1C">Item 1C</a></li>
      <li><a href="#Item-1D">Item 1D</a></li>
      <li><a href="#Item-1E">Item 1E</a></li>
    </ul>
  </li>
  <li>
    <a href="#">Item 2</a>
    <ul class="menu">
      <li><a href="#Item-2A">Item 2A</a></li>
      <li><a href="#Item-2B">Item 2B</a></li>
      <li><a href="#Item-2C">Item 2C</a></li>
      <li><a href="#Item-2D">Item 2D</a></li>
      <li><a href="#Item-2E">Item 2E</a></li>
    </ul>
  </li>
  <li>
    <a href="#">Item 3</a>
    <ul class="menu">
      <li><a href="#Item-3A">Item 3A</a></li>
      <li><a href="#Item-3B">Item 3B</a></li>
      <li><a href="#Item-3C">Item 3C</a></li>
      <li><a href="#Item-3D">Item 3D</a></li>
      <li><a href="#Item-3E">Item 3E</a></li>
    </ul>
  </li>
  <li><a href="#Item-4"> Item 4</a></li>
</ul>

## autoHeight

<div class="secondary callout">
  <p>If you like to set the height to auto you can also set the autoHeight and animateHeight params</p>
  <button class="button expanded" onclick="$('#m3').foundation('destroy');if($('#m3').data('autoHeight')){$('#m3').data('autoHeight',false);$(this).html('autoHeight is Off');}else{$('#m3').data('autoHeight',true);$(this).html('autoHeight is On');}new Foundation.Drilldown($('#m3'));return false;">autoHeight is On</button>
</div>

<ul class="menu" data-drilldown data-auto-height="true" data-animate-height="true" style="width: 200px" id="m3">
  <li>
    <a href="#">Item 1</a>
    <ul class="menu">
      <li>
        <a href="#">Item 1A</a>
        <ul class="menu">
          <li><a href="#Item-1Aa">Item 1Aa</a></li>
          <li><a href="#Item-1Ba">Item 1Ba</a></li>
        </ul>
      </li>
      <li><a href="#Item-1B">Item 1B</a></li>
      <li><a href="#Item-1C">Item 1C</a></li>
      <li><a href="#Item-1D">Item 1D</a></li>
      <li><a href="#Item-1E">Item 1E</a></li>
    </ul>
  </li>
  <li>
    <a href="#">Item 2</a>
    <ul class="menu">
      <li><a href="#Item-2A">Item 2A</a></li>
      <li><a href="#Item-2B">Item 2B</a></li>
      <li><a href="#Item-2C">Item 2C</a></li>
      <li><a href="#Item-2D">Item 2D</a></li>
      <li><a href="#Item-2E">Item 2E</a></li>
    </ul>
  </li>
  <li>
    <a href="#">Item 3</a>
    <ul class="menu">
      <li><a href="#Item-3A">Item 3A</a></li>
      <li><a href="#Item-3B">Item 3B</a></li>
      <li><a href="#Item-3C">Item 3C</a></li>
      <li><a href="#Item-3D">Item 3D</a></li>
      <li>
        <a href="#Item-3E">Item 3E</a>
        <ul class="menu">
          <li><a href="#Item-3EA">Item 3EA</a></li>
          <li><a href="#Item-3EB">Item 3EB</a></li>
          <li><a href="#Item-3EC">Item 3EC</a></li>
          <li><a href="#Item-3ED">Item 3ED</a></li>
          <li><a href="#Item-3EE">Item 3EE</a></li>
          <li><a href="#Item-3EA">Item 3EA</a></li>
          <li><a href="#Item-3EB">Item 3EB</a></li>
          <li><a href="#Item-3EC">Item 3EC</a></li>
          <li><a href="#Item-3ED">Item 3ED</a></li>
          <li><a href="#Item-3EE">Item 3EE</a></li>
          <li><a href="#Item-3EA">Item 3EA</a></li>
          <li><a href="#Item-3EB">Item 3EB</a></li>
          <li><a href="#Item-3EC">Item 3EC</a></li>
          <li><a href="#Item-3ED">Item 3ED</a></li>
          <li><a href="#Item-3EE">Item 3EE</a></li>
        </ul>
      </li>
    </ul>
  </li>
  <li><a href="#Item-4"> Item 4</a></li>
  <li><a href="#Item-5"> Item 5</a></li>
  <li><a href="#Item-6"> Item 6</a></li>
  <li><a href="#Item-7"> Item 7</a></li>
  <li><a href="#Item-8"> Item 8</a></li>
</ul>

## ScrollTop Drilldown

<div class="callout">Scroll to the top of the menu when selecting a submenu/navigating back using the menu back button. Can be useful with a longer menu to provide a better user experience.</div>

<ul class="menu" data-drilldown data-scroll-top="true" style="width: 200px" id="m2">
  <li><a href="#">Item</a></li>
  <li><a href="#">Item</a></li>
  <li><a href="#">Item</a></li>
  <li><a href="#">Item</a></li>
  <li><a href="#">Item</a></li>
  <li><a href="#">Item</a></li>
  <li><a href="#">Item</a></li>
  <li><a href="#">Item</a></li>
  <li><a href="#">Item</a></li>
  <li><a href="#">Item</a></li>
  <li> <a href="#">Item</a>
    <ul class="vertical menu">
      <li><a href="#">Item</a></li>
      <li><a href="#">Item</a></li>
      <li><a href="#">Item</a></li>
      <li><a href="#">Item</a></li>
      <li><a href="#">Item</a></li>
      <li><a href="#">Item</a></li>
      <li><a href="#">Item</a></li>
      <li><a href="#">Item</a></li>
      <li><a href="#">Item</a></li>
      <li><a href="#">Item</a></li>
      <li><a href="#">Item</a></li>
      <li><a href="#">Item</a></li>
      <li><a href="#">Item</a></li>
      <li><a href="#">Item</a></li>
      <li><a href="#">Item</a></li>
      <li><a href="#">Item</a></li>
      <li><a href="#">Item</a></li>
      <li><a href="#">Item</a></li>
      <li><a href="#">Item</a></li>
      <li><a href="#">Item</a></li>
      <li><a href="#">Item</a></li>
      <li><a href="#">Item</a></li>
      <li><a href="#">Item</a></li>
      <li><a href="#">Item</a></li>
      <li><a href="#">Item</a></li>
      <li><a href="#">Item</a></li>
      <li><a href="#">Item</a></li>
      <li><a href="#">Item</a></li>
      <li><a href="#">Item</a></li>
      <li> <a href="#">Item</a>
        <ul class="vertical menu">
          <li><a href="#">Item</a></li>
        </ul>
      </li>
    </ul>
  </li>
  <li><a href="#">Item</a></li>
</ul>

---

## Custom Styling

The drilldown plugin automatically adds a back button to the top of each nested menu. To style this control, target the `.js-drilldown-back` class:

```css
.js-drilldown-back {
  // ...
}
```
