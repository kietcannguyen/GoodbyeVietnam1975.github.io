---
layout: post
title: "Family Tree"
categories: misc
---

{% raw %}
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Family Tree</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      margin: 20px;
    }

    .family-tree {
      display: flex;
      justify-content: center;
    }

    .person {
      text-align: center;
      margin: 20px;
    }

    .generation {
      margin-bottom: 40px;
    }

    .spouse::before {
      content: "❤";
    }
  </style>
</head>
<body>

  <div class="family-tree">

    <div class="generation">
      <div class="person">Grandfather</div>
      <div class="person spouse">Grandmother</div>
    </div>

    <div class="generation">
      <div class="person">Father</div>
      <div class="person spouse">Mother</div>
      <div class="person">Uncle</div>
    </div>

    <div class="generation">
      <div class="person">You</div>
      <div class="person spouse">Spouse</div>
      <div class="person">Sibling</div>
      <div class="person spouse">Sibling's Spouse</div>
    </div>

    <div class="generation">
      <div class="person">Child 1</div>
      <div class="person">Child 2</div>
    </div>

  </div>

</body>
</html>
{% endraw %}
