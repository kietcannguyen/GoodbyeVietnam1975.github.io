---
layout: post
title: "Family Tree"
categories: misc
---

{% raw %}
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

    .tree {
      display: flex;
      justify-content: center;
      align-items: center;
      height: 100vh;
    }

    .node {
      text-align: center;
      margin: 20px;
      position: relative;
    }

    .node::before {
      content: "";
      position: absolute;
      top: -20px;
      left: 50%;
      width: 0;
      height: 20px;
      border-style: solid;
      border-width: 1px;
      border-color: black;
    }

    .node.left::before {
      border-left: none;
      border-right: 20px solid black;
      transform: translateX(-50%);
    }

    .node.right::before {
      border-left: 20px solid black;
      border-right: none;
      transform: translateX(-50%);
    }

    .child-container {
      display: flex;
    }
    
    .child-container > .node {
      flex: 1;
    }
  </style>
</head>
<body>

  <div class="tree">
    <div class="node">
      <div>Grandfather</div>
      <div class="child-container">
        <div class="node left">
          <div>Father</div>
          <div class="child-container">
            <div class="node left">
              <div>Child 1</div>
              <div class="child-container">
                <div class="node left"><div>Grandchild 1</div></div>
                <div class="node right"><div>Grandchild 2</div></div>
              </div>
            </div>
            <div class="node right">
              <div>Child 2</div>
              <div class="child-container">
                <div class="node left"><div>Grandchild 3</div></div>
                <div class="node right"><div>Grandchild 4</div></div>
              </div>
            </div>
          </div>
        </div>
        <div class="node right">
          <div>Uncle</div>
        </div>
      </div>
    </div>
  </div>

</body>
</html>
{% endraw %}

