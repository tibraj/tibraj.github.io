---
layout: post
title:      "Js Project"
date:       2020-10-13 15:46:20 +0000
permalink:  js_project
---

For theJavaScript project, I built an application that allows users to create a list for household chores and remove whichever one based on completion. My favorite lines of code appear in the the chore.js file:

```
document.querySelectorAll('.chore-button').forEach(element => {
          element.addEventListener('click', deleteChore)
};
```

These few lines appear at the end of a function fetching the chores a user has created. They encapsulate multiple facets of the JavaScript section I was recently introduced to: dom traversal, event listeners and the invocation of functions within a function. The simplicity of the user's interaction with the delete button belies the complexity with which its process dynamically unifies different concepts.



