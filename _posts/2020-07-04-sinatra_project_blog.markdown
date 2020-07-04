---
layout: post
title:      "Sinatra Project Blog"
date:       2020-07-04 18:03:36 +0000
permalink:  sinatra_project_blog
---


After completing my Sinatra project, I found that the piece of code I favored the most was the has_secure_password macro in my Users model. The reason for this is that it simultaneously encourages laziness and further research. It accomplishes so much implicitly that one's assurance of password security and validation seems like an afterthought belittling its multifaceted function if one were to comprehensively put it in words. This feels like a microcosm of the entire project; specifically, the constant back and forth between controllers, views and the browser itself. The incessant possibility of being decentered, or losing track of one's thinking or development belies the brevity with which one can describe the idea that a user can see all posts on a website but can only edit and delete his own. While reviewing my project multiple times, I'd have the tendency to skirt past the has_secure_password macro by ending with the notion that I can use the authenticate method. Really, the bcrypt gem is used along with the password_digest attribute in my database table. The gem retrieves a stored salt and key from ciphered text within the attribute and encrypts the unencrypted password submitted by the user. These are compared to see if they match and are authenticated if they do. I realized I was encountering the first algorithm in my nascent progamming life and was spending more time learning about areas I'm still uncomfortable with, such as the Gemfile.

```
class User < ActiveRecord::Base

    has_secure_password
		
end
```
