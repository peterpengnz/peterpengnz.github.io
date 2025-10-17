---
layout: post
title: "What will you do with Next Method in Ruby String#?"
date: 2025-10-17 10:00:00 +0000
---

# 🔍 Exploring Ruby's `String#next` Method

Ruby’s `String#next` (also known as `succ`) is a surprisingly powerful method that can increment strings in intuitive and sometimes unexpected ways. Whether you're working with numbers, letters, or even special characters, `next` can be a handy tool in your Ruby toolkit.

---

## 🧠 What Is `String#next`?

The `next` method returns the successor to a string. It’s part of Ruby’s `String` class and is often used to increment strings in a way that mimics counting.

### Examples:

```ruby
"1".next     # => "2"
"9".next     # => "10"
"a".next     # => "b"
"z".next     # => "aa"
"9z".next    # => "a0"
"z9".next    # => "aa0"
"!".next     # => "\""
"ZZ".next    # => "AAA"
```

### 📚 Related Methods

Ruby provides four related methods:

- `next`
- `next!`
- `succ`
- `succ!`

The non-bang versions return a new string, while the bang versions modify the original string in place.

### 🔢 Numeric Strings

```
"9".next     # => "10"
"99".next    # => "100"
```

Ruby treats numeric strings like counters, rolling over digits as needed.

### 🔤 Alphabetic Strings

```
"a".next # => "b"
"z".next # => "aa"
"az".next # => "ba"
"zz".next # => "aaa"
```

Just like an odometer, letters roll over from z to aa, az to ba, and so on.

### 🔡 Alphanumeric Strings

```
"1a".next # => "1b"
"1z".next # => "2a"
"1az".next # => "1ba"
"1aaz".next # => "1aba"
"z9".next # => "aa0"
```

Ruby handles mixed strings with surprising intelligence, incrementing the rightmost alphanumeric segment.

### 🔣 Special Characters

```
"!".next # => "\""
"~".next # => "\u007F" # DEL in ASCII
"".next # => ""
```

Even special characters follow ASCII progression. The empty string remains unchanged.

### 🤔 Why Use String#next?

- Generate unique IDs or codes
- Create alphabetical pagination
- Build custom counters
- Explore ASCII behavior in strings

### 📎 References

- [Ruby API: String#succ](https://rubyapi.org/3.4/o/string#method-i-succ)
- [ASCII Table – Wikipedia](https://en.wikipedia.org/wiki/ASCII)
- [ASCII Code Reference](https://www.ascii-code.com/)

### Youtube Video

Checkout my video about this in Chinese:
Ruby 里面有趣的 String#next 方法（也叫 String#succ）

<iframe width="560" height="315" src="https://www.youtube.com/embed/5h9RM_2WSxQ?si=mtyA0abqjva2yfHj" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>
