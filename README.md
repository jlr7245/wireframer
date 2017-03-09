# Wireframer

A package that dynamically generates HTML layouts and the corresponding CSS based on command line inputs.

```bash
wireframer layout:new "home" --flexbox
wireframer "home":addrow(1) "hero"(div):full
wireframer "home":addrow(2) "features"(div):in-grid:col-3:"feature"(li)
wireframer "home":addrow(3) "content"(main):in-grid:col-1:p
wireframer "home":addrow(4) "footer"(footer):full:col-4:"footer-col"(div)
```

might evaluate to

```html

<div class='hero'></div>

<div class='w--in-grid'>
  <div class='features'>
    <ul>
      <li class='feature'></li>
      <li class='feature'></li>
      <li class='feature'></li>
    </ul>
  </div>
</div>

<div class='w--in-grid'>
  <main class='content'>
    <p></p>
  </main>
</div>

<footer class='footer'>
  <div class='footer-col'></div>
  <div class='footer-col'></div>
  <div class='footer-col'></div>
  <div class='footer-col'></div>
</footer>

```