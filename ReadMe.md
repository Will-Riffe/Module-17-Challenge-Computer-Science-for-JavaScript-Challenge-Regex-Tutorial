# Learn how to Match an Email Using Regex

## 💡 Let's Go! 💡

Here, we check out a regular expression— aka, regex —for matching an email address. 
Regex are character sequences which define specific search patterns, 
and are used in programming when we are trying to find patterns in strings.

Regex can look a little like this:

```javascript
/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/
```

In fact, the above regex is what we'll be focusing on in this article. 
Below, we'll deconstruct this seemingly jumbled mass of charactars in order
to better 


## 1. The ^ Symbol
The `^` (i.e. the circumflex, or 'anchor' in this case) is a symbol which starts the regex line, or string. In our case, it indicates that the email address should start at the beginning of the string.

