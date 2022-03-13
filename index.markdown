---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: default copy
title: Garden & Fun
---
<style>
div.slide-down {
  width:100%;
  overflow:hidden;
}
div.slide-down h1 {
  animation: 5s slide-down;
  margin-top: 40%;
}

@keyframes slide-down {
  from {
    margin-top: -50%;
    height: 300%; 
  }

  to {
    margin-top: 40%;
    height: 100%;
  }
}
</style>

<div class="slide-down">

<h1>Welcome to Garden & Fun!</h1>
<p><a href="/about.html"> About</a> | <a href="/blog.html">Blog</a> | <a href="/staff.html">Staff</a></p>
</div>