<h1 align="center">
  Regular Expression Compendium
</h1>
<h5 align="center">(in the making)</h5>

<p align="center">
<a href="https://github.com/baronblue/regular-expression-compendium/blob/master/LICENSE" target="blank">
<img src="https://img.shields.io/github/license/baronblue/regular-expression-compendium?style=flat-square" alt="regular-expression-compendium license" />
</a>
<a href="https://github.com/baronblue/regular-expression-compendium/fork" target="blank">
<img src="https://img.shields.io/github/forks/baronblue/regular-expression-compendium?style=flat-square" alt="regular-expression-compendium forks"/>
</a>
<a href="https://github.com/baronblue/regular-expression-compendium/stargazers" target="blank">
<img src="https://img.shields.io/github/stars/baronblue/regular-expression-compendium?style=flat-square" alt="regular-expression-compendium stars"/>
</a>
<a href="https://github.com/baronblue/regular-expression-compendium/issues" target="blank">
<img src="https://img.shields.io/github/issues/baronblue/regular-expression-compendium?style=flat-square" alt="regular-expression-compendium issues"/>
</a>
<a href="https://github.com/baronblue/regular-expression-compendium/pulls" target="blank">
<img src="https://img.shields.io/github/issues-pr/baronblue/regular-expression-compendium?style=flat-square" alt="regular-expression-compendium pull-requests"/>
</a>
</p>

<p align="center">
    ·
    <a href="https://github.com/baronblue/regular-expression-compendium/issues/new/choose">Report Bug</a>
    ·
    <a href="https://github.com/baronblue/regular-expression-compendium/issues/new/choose">Request Feature</a>
    ·
    <a href="https://github.com/baronblue/regular-expression-compendium/issues/new/choose">Submit Expression</a>
    ·
</p>

## Introduction

I'm compiling a list of all the regular expressions that I find helpful, and I think you may too.

## How to use it?

If you want to test the expressions you can always go to [regex101](https://regex101.com). The website is amazing.

If you use Visual Studio Code I recommend downloading the [Regexp Explain](https://marketplace.visualstudio.com/items?itemName=LouisWT.regexp-preview). The preview is amazing.

<img src="https://i.loli.net/2017/08/18/59968e8dde40c.gif">

<h5 align="center">image from the publisher</h5>

Here are some ways to use it.

### Code Samples

I'll include the code samples for each regular expression. I'll use python but if you **don't see your favorite programing language please <a href="https://github.com/baronblue/regular-expression-compendium/issues/new/choose">submit an code sample</a> and I'll add it with full attribution of course :).**

---

## The list

The list is separated in various sections. I can change the order or you can propose one that makes more sense. Feedback is welcome.

- [Dates](#dates)
- [Types](#types)
- [Check format](#format)
- [HTML](#html)
- [Colors](#colors)

### Dates

### Types

Is a number (positive only)?

```regex
^\d+$
```

Is a number (optional negative)?

```regex
^-?\d+$
```

Is a decimal number (positive only)?

```regex
^\d+.?\d+$
```

Is a decimal number (optional negative)?

```regex
^-?\d+.?\d+$
```

Is a binary number?

```regex
\A[01]+\Z
```

### Format

Is an email?

```regex
(?:[a-z0-9!#$%&'*+/=?^_`{|}~-]+(?:\.[a-z0-9!#$%&'*+/=?^_`{|}~-]+)*|"(?:[\x01-\x08\x0b\x0c\x0e-\x1f\x21\x23-\x5b\x5d-\x7f]|\\[\x01-\x09\x0b\x0c\x0e-\x7f])*")@(?:(?:[a-z0-9](?:[a-z0-9-]*[a-z0-9])?\.)+[a-z0-9](?:[a-z0-9-]*[a-z0-9])?|\[(?:(?:25[0-5]|2[0-4][0-9]|[01]?[0-9][0-9]?)\.){3}(?:25[0-5]|2[0-4][0-9]|[01]?[0-9][0-9]?|[a-z0-9-]*[a-z0-9]:(?:[\x01-\x08\x0b\x0c\x0e-\x1f\x21-\x5a\x53-\x7f]|\\[\x01-\x09\x0b\x0c\x0e-\x7f])+)\])
```

<h5 align="center">I don't remember where I got this one. If it's yours, please contact me to add the appropriate referral</h5>

Is an URL?

```regex
((www\.|(http|https|ftp|news|file)+\:\/\/)[_.a-z0-9-]+\.[a-z0-9\/_:@=.+?,##%&~-]*[^.|\'|\# |!|\(|?|,| |>|<|;|\)])/
```

<h5 align="center">I don't remember where I got this one. If it's yours, please contact me to add the appropriate referral</h5>

Is a credit card?

```regex
^(?:4[0-9]{12}(?:[0-9]{3})?|5[1-5][0-9]{14}|6011[0-9]{12}|622((12[6-9]|1[3-9][0-9])|([2-8][0-9][0-9])|(9(([0-1][0-9])|(2[0-5]))))[0-9]{10}|64[4-9][0-9]{13}|65[0-9]{14}|3(?:0[0-5]|[68][0-9])[0-9]{11}|3[47][0-9]{13})*$
```

<h5 align="center">I don't remember where I got this one. If it's yours, please contact me to add the appropriate referral</h5>

Is a IP V4?

```regex
^(?:(?:25[0-5]|2[0-4][0-9]|[01]?[0-9][0-9]?)\.){3}(?:25[0-5]|2[0-4][0-9]|[01]?[0-9][0-9]?)$
```

<h5 align="center">I don't remember where I got this one. If it's yours, please contact me to add the appropriate referral</h5>

Is a IP V6?

```regex
^(([0-9a-fA-F]{1,4}:){7,7}[0-9a-fA-F]{1,4}|([0-9a-fA-F]{1,4}:){1,7}:|([0-9a-fA-F]{1,4}:){1,6}:[0-9a-fA-F]{1,4}|([0-9a-fA-F]{1,4}:){1,5}(:[0-9a-fA-F]{1,4}){1,2}|([0-9a-fA-F]{1,4}:){1,4}(:[0-9a-fA-F]{1,4}){1,3}|([0-9a-fA-F]{1,4}:){1,3}(:[0-9a-fA-F]{1,4}){1,4}|([0-9a-fA-F]{1,4}:){1,2}(:[0-9a-fA-F]{1,4}){1,5}|[0-9a-fA-F]{1,4}:((:[0-9a-fA-F]{1,4}){1,6})|:((:[0-9a-fA-F]{1,4}){1,7}|:)|fe80:(:[0-9a-fA-F]{0,4}){0,4}%[0-9a-zA-Z]{1,}|::(ffff(:0{1,4}){0,1}:){0,1}((25[0-5]|(2[0-4]|1{0,1}[0-9]){0,1}[0-9])\.){3,3}(25[0-5]|(2[0-4]|1{0,1}[0-9]){0,1}[0-9])|([0-9a-fA-F]{1,4}:){1,4}:((25[0-5]|(2[0-4]|1{0,1}[0-9]){0,1}[0-9])\.){3,3}(25[0-5]|(2[0-4]|1{0,1}[0-9]){0,1}[0-9]))$
```

<h5 align="center">I don't remember where I got this one. If it's yours, please contact me to add the appropriate referral</h5>

### HTML

Is a HTML tag?

```regex
^<([a-z]+)([^<]+)*(?:>(.*)<\/\1>|\s+\/>)$
```

Is an image HTML tag?

```regex
^<\s*img[^>]+src\s*=\s*(["'])(.*?)\1[^>]*>$
```

### Colors

Is an Hex?

```regex
^#?([a-f0-9]{6}|[a-fA-F0-9]{3})$
```

### Country Specific

Some expressions only make sense for certain countries, like phone number formats, zip codes, etc.

#### Portugal 🇵🇹

Valid phone number. Here are the valid ways to display the number:

- +351 ### ### ###
- 00 351 ### ### ###

```regex
^(\+351\s?|[0]{2}\s?351\s?)?\d{3}\s?\d{3}\s?\d{3}
```

Our country code is 351 and all phone numbers have 9 numbers. We can have optionally spaces between each set of 3.

---

## 🙏 Thanks to

I'm not creating all the expressions, so I'll feature the authors of each. If you have an expression that you want to submit, don't forget to include your social or website to thank you here.

---

## 💪 Contributing

Expressions are always welcome, so please <a href="https://github.com/baronblue/regular-expression-compendium/issues/new/choose">Submit an Expression</a>. I'll check it, and if it makes sense, I'll add it. Please don't forget to include what's it supposed to test for, so that I can understand it better.

<hr>
<p align="center">
Made in ☀️ Portugal with ❤️
</p>
