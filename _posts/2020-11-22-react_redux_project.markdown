---
layout: post
title:      "React/Redux Project"
date:       2020-11-22 23:43:50 +0000
permalink:  react_redux_project
---


For the React/Redux project, I built an application with signup and login functionality that allows users to create, post and delete essays. My favorite line of code appears in the frontend of the project:

```
export default connect(mapStateToProps, {updateEssayForm, createEssay})(EssayForm)
```

This line of code returns a higher order React component class, building props from the store state and passing them into the component. All client level logic is handled here and no changes are made to the component class passed into the connect function. The heavy work is done implicitly.
