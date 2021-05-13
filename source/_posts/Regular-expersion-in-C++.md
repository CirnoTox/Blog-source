---
title: Regular expersion in C++
date: 2021-05-10 07:41:54
tags:
---
This post mainly talks about the grammar and usage of `Regular Expersion` in C++.
# Grammar
 The grammar is specified by the use of `std::regex_constants::syntax_option_type` enumeration values.They are defined in `std::regex_constants`:
 * ECMAScript(default)
 * basic
 * extended
 * awk
 * grep
 * egrep
 Only one of above grammars can be specified.

 Several others flags can be applied at the same time:
 * icase
 * nosubs
 * optimize
 * collate
## Element
An element can be one of the following things:
* An ordinary character
* A wildcard character '.' that matches any character except a newline.
* A bracket expression of the form "[expr]",or of the form "[^expr]".
* An anchor '^' or '$'.
* An identity escape of the form "\k", which matches the character k.