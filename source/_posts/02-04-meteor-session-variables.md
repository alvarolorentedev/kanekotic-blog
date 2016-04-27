---
title: Meteor - Session variables
date: 2016-02-04 20:22:36
tags: daily, learn
---

Session variables are easy to use in meteor. the can ve get and set from the javascript code using:

```javascript
Session.get('variableName');
Session.set('variableName', true);
```

on your HTML you can reference the get method easily by:
```HTML
<template name="admin">
    {{#if $.Session.get 'variableName'}}
        I am here
    {{else}}
        I am not here
    {{/if}}
</template>
```
