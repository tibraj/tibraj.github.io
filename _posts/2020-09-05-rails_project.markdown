---
layout: post
title:      "Rails Project"
date:       2020-09-05 15:20:18 +0000
permalink:  rails_project
---


For the rails project, I built an application that allows users to write essays as well as respond to other users' essays. My favorite line of code appears in the essay model: 

```
scope :recent, lambda { where('created_at >= ?', Time.now - 1.week) }
```

This scope method provides reevaluation and, in tandem with the corresponding 'recent' method in my essays controller: 

```
def recent 
        @essays = Essay.all.recent
end
```

I'm able to provide a page in my application that reflects constant change according to user activity. Older essays maintain their home in the index page for essays while newly created ones are highlighted on the recent page for essays. Supposing regular user activity, a facet of the application will present something different on a weekly base.
