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


## 1. The ^ Symbol- an Anchor
    The `^` (i.e. the circumflex, or 'anchor' in this case) is a symbol which starts the regex line, or string. In our case, it indicates that the email address should start at the beginning of the string.

## 2. Bracket Expressions
    The '[]' is used to contain sets of characters, or specifically, charactar classes. 

## 3. Charactar Classes
    Character classes define what charactars may be used. 

### 3.1 The Username Component
    This is the username component: `[a-z0-9_\.-]+` 

    In the Email matching Regex, the username component matches characters of the username portion of an email address may contain. In the brackets, the Username Component accounts for lowercase letters, digits, underscores, periods, and hyphens.

## 4. Quantifiers
    Quantifiers are what regular expressions use to declare an expectation of something to match (ex '+'), though they can also declare how many charactars there may be (ex '{2,6}').

### 4.1 Domain Component
    This is the domain component `[\da-z\.-]+` 

    Separated from the Username component by th '@' symbol, this 'quantifier' lists a range of characters which may appear in the domain portion of an email address. As you can see, it allows lowercase letters, periods, and hyphens;  the `+` symbol, the quantifier, is a stated requirement that at least one of the listed characters are present.

### 4.2 TLD Component
    The TLD (Top-Level Domain) component `[a-z\.]{2,6}` 

    This is where the typical '.com', '.net', etc could be expected. This quantifier matches the characters which can appear in the domain extension of an email address— allowing for lowercase letters and periods; the `{2,6}` quantifier specifies the TLD to be two to six characters long.