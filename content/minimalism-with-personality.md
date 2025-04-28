+++
title = "Minimalism with Personality"
date = 2025-02-20T23:43:37+05:45
[taxonomies] 
tags = ["articles"]
+++

Modern logos and design rely heavily on simplification of everything.
This site being one of the examples. I do like a minimalistic design.
But when it comes to uniqueness and personality of something, things
turn a different way. The more minimal we go the more general and bland
it gets. It'll lack the [_personality_] of it to show it's difference
from others. While a maximalist approach would include tiniest of details
to make it more unique and personal than ever, a minimal design would take
some very clever tricks to achieve uniqueness.

This site is directly inspired by [manu](https://manuelmoreale.com/)'s
site but I wanted to add my own touch to it as he also has given to it.
I wouldn't say his site lacks personality because I loved the design and
the minimalistic approach of his site that I wanted one for myself too.
But, to make my site more personal and unique in itself I added a handwriting
style text for my inner voice [_inner voice... [_inner voice..._]_] for the
things I think while writing.

Take a look at this logo. It is made up of completely straight lines. It's
minimal as well as unique. [_This is scientiac's logo and he talks about it
whenever he gets the chance to. He is very proud of it._]

<div align="center">
<select id="themeSelect" style="appearance: none; text-align: center;">
  <!-- Everforest -->
  <option value="everforest-light">Everforest Light</option>
  <option value="everforest-dark">Everforest Dark</option>
  <!-- Gruvbox -->
  <option value="gruvbox-light">Gruvbox Light</option>
  <option value="gruvbox-dark">Gruvbox Dark</option>
  <!-- Night -->
  <option value="night-solis">Night Solis</option>
  <option value="night-spaceduck">Night Spaceduck</option>
  <option value="night-gotham">Night Gotham</option>
  <!-- Nord -->
  <option value="nord">Nord</option>
  <!-- One -->
  <option value="one-light">One Light</option>
  <option value="one-dark">One Dark</option>
  <!-- Catppuccin -->
  <option value="catppuccin-latte">Catppuccin Latte</option>
  <option value="catppuccin-frappe">Catppuccin Frappe</option>
  <option value="catppuccin-macchiato">Catppuccin Macchiato</option>
  <option value="catppuccin-mocha">Catppuccin Mocha</option>
</select>
</div>
<!-- Image element. The src URL includes the selected theme in its name -->
<img id="themeImage" src="https://scientiac.space/res/colors/logo-everforest-light.svg" style="width:40%;" alt="Theme logo">

<script>
  // Get references to the select element and image
  const themeSelect = document.getElementById('themeSelect');
  const themeImage = document.getElementById('themeImage');

  // Update image based on the user's theme selection
  themeSelect.addEventListener('change', function() {
    const selectedTheme = themeSelect.value;
    // Construct the new image URL using the selected theme
    const newUrl = `https://scientiac.space/res/colors/logo-${selectedTheme}.svg`;
    themeImage.style.opacity = 0;
    setTimeout(() => {
      themeImage.src = newUrl;
      themeImage.style.opacity = 1;
    }, 200);
  });
</script>

But, thinking about personality, I sometimes wish that apples were rainbow
colored and the window glasses were tinted with colors.

[_A colorful place for colorful minds._]

But, [_("but" strikes back)_]  I love a good minimalist approach of things.
I like the new mozilla logo. I like the fact how the new Pepsi's logo look
and yes I do love GNOME's foot. [_(Wouldn't call it a fetish though. XD)_]

[_Because they have their quirks and their own personalities._]
