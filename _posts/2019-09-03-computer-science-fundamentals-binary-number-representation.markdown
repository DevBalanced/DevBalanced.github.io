---
layout: post
title: "CS Fundamentals II: Binary"
date: 2019-09-03
description: Basics of binary number representation. # Add post description (optional)
img: cs-fundamentals/binary/postimage.jpg # Add image post (optional)
---

Hi!

This post is the second in the CS Fundamentals series, todays topic is a concept which forms the basis for all modern computer systems. The binary number system! Hopefully this post will give someone with little understanding of the topic a better idea of why it is so important.

---

# Contents
1. [What is binary?](#what_is_binary)
	1. [Encoding](#encoding)
	2. [Binary units](#binary_units)
2. [How binary works](#how_binary_works)
	1. [Base-2 and base-10](#base-2_base-10)
	2. [Place values](#place_values)
	3. [Comparison](#comparison)
	4. [Why do we use binary?](#why_binary)
3. [Converting denary to binary](#conversion)
	1. [Divide by 2 method](#div_2)
	2. [Largest place value method](#largest_place)
4. [Conclusion](#conclusion)
	1. [This post](#this_post)
	2. [Next post](#next_post)

---

# What is binary? <a name="what_is_binary"></a>

Binary - most people think of it as 1s and 0s, and they are correct but there is a lot more to it than that! The binary number system is another method of representing numbers which uses *bits* (BInary digiTS), a single bit can be either a 1 or a 0. An example of a binary number could be 101.

The CPU (Central Processing Unit) of your computer is made up of billions of tiny electrical components called *transistors*. A transistor is a switch that when activated switches between one of two states - on or off. These states correspond to the 1 and 0 of a binary number. A simple explanation of how a transistor works and why it is so useful can be found on the simple wikipedia [here][wiki-link].

In the previous post we mentioned that source code, i.e code written in a programming language, is compiled down into machine code - which is binary. The CPU can read these instructions which correspond to basic commands that the CPU then carries out, for example adding two numbers or loading a number from memory.

## Encoding <a name="encoding"></a>

All the files on your computer whether they are audio, video, documents etc are all stored as binary. All the information that is processed by a computer is done so in binary. However we dont usually see 1s and 0s due to a process called *encoding*. 

There are several ways that computers encode information. One easy to understand example is text - individual characters correspond to a mapping from characters to numbers and guess what, the numbers are stored as binary. You may have heard of ASCII or Unicode, these are character encoding standards. Check out the ASCII table below from [IBM][ibm-link].

![ASCII Table](/assets/img/cs-fundamentals/binary/ascii_table.jpg)

Another encoding is going on in the monitor that you are using to read this very post. Each pixel is made up of three sub-pixels that correspond to the red, green and blue channels in the RGB color model. By varying the intensity of each channel different colors can be created - like mixing paint. Each intensity value is stored as binary!

I took the image below on my phone while writing this, if you zoom in on an LCD screen enough the sub-pixels begin to become visible.

![RGB diagram](/assets/img/cs-fundamentals/binary/rgb.jpg){:height="250px" width="250px" .center-image}

Encoding has become standardized over time, this promotes compatibility between different types of computers (operating systems etc):
- Audio file formats: WAV, AAC, OGG
- Image: JPEG, PNG, GIF
- Video: MPEG4

Additionally the more bits that are used then the larger the range of values (as the maximum binary number is larger), therefore a larger number of items can be encoded. Using the ASCII and Unicode example, ASCII uses 8-bits this means the maximum number of characters it can map is 128. Unicode has a variety of encodings which can support up to 32-bits, offering a mapping of theoretically millions of characters. This is calculated using 2<sup>number of bits</sup>, so 2<sup>8</sup> = 128 different characters.

## Binary units <a name="binary_units"></a>

Often when talking about bits it is easier to group them together into *bytes*. There is 8 bits in a byte. Other groupings exist such as a *nibble* which is 4 bits, and you are probably familiar with kilobytes, megabytes, gigabytes and terabytes from reading computer specifications. These unit prefixes work as they do for other units, a kilobyte is roughly 1000 bytes. I say roughly as the actual number is 1024 and this is because binary is a base-2 number system. What is a base-2 number system? Read on.

![Bytes diagram](/assets/img/cs-fundamentals/binary/bytes.jpg){: .center-image}

---

# How binary works <a name="how_binary_works"></a>

## Base-2 and base-10 <a name="base-2_base-10"></a>

The binary number system, also called the base-2 number system, is a number system where the number is represented using only two symbols, we use 1 and 0. Compare this to the decimal number system that we are all familiar with where a number is represented with ten symbols, we use 0 through 9. The decimal system is also known as denary or base-10. The base of the number system, also known as a radix, is the number of different digits that can be used to represent numbers, hence base-2 and base-10.

![Radix diagram](/assets/img/cs-fundamentals/binary/radix.jpg)

## Place values <a name="place_values"></a>

As mentioned prior each digit in a binary number is called a *bit*, this is a portmanteau of the words binary and digit. By using multiple bits we can represent more numbers than just 1 or 0, we do this in exactly the same way that we do in base-10. In base-10 each place value corresponds to a power of 10, starting at 0. As anything to the power 0 is 1, the first is always 1 (individual units). Think back to being very young and learning the 1s, 10s, 100s, 1000s place names. In binary each place value corresponds to a power of 2 instead of 10 - 1s, 2s, 4s, 8s and so forth.

![Place values diagram](/assets/img/cs-fundamentals/binary/placevalues.jpg)

## Comparison <a name="comparison"></a>

Lets compare the representations by representing the same number in both binary and denary, lets use the number 135.

![Comparison diagram](/assets/img/cs-fundamentals/binary/comparison.jpg)

So to represent the number 135 in binary you use 10000111. For us that string of 1s and 0s is more difficult to understand, so the next question is why would you use binary?

## Why do we use binary? <a name="why_binary"></a>

The reason that binary is used in computers is its simplicity, as each digit in a binary number can only be in one of two states - 1 or 0. This corresponds with an electrical signal being either on or off. When numbers are stored in your computer they are an electrical signal (think of the transistors mentioned earlier), if we wanted to represent the number in denary then we would have to be able to differentiate between multiple different levels of voltage. Naturally this would lead to ambiguity, if the voltage is either on or off there is no risk of the signal being interpreted incorrectly. I like to visualize the signal like this:

![Signal diagram](/assets/img/cs-fundamentals/binary/signal.jpg)

As you can see even if the signal is distorted, it is still possible to read the signal and retrieve the information. If this signal had several different discrete levels then the chance of the distortion affecting the signal is greater.

---

# Converting denary to binary <a name="conversion"></a>

## Divide by 2 method <a name="div_2"></a>

Typically if you want to convert between denary and binary I would recommend using a calculator as it is much faster and there is no chance of making mistakes, however it does help to reinforce the understanding of the concept by working through an example of conversion. The way that I was taught is the "divide by 2" method. You take the denary number and divide it by 2, writing down the remainder as you go. Once youve finished you reverse the number. Lets try this on the number 96.


![Remainder diagram](/assets/img/cs-fundamentals/binary/remainder.jpg)

## Largest place value method <a name="largest_place"></a>

We see now what is happening with this method - first the largest possible place value is set to 1 in the binary number, then subtract this place value from the number you are converting and move from left to right through the binary number looking for the next largest potential place value given the remaining amount. This illustration will make it clear what I mean, using the number 100.

![Conversion diagram](/assets/img/cs-fundamentals/binary/conversion.jpg)

Another thing you might have noticed is that for binary numbers, if they are odd the last place value will always be 1 and even numbers the last place will always be 0. This is clearly because the place value is 1!

---

# Conclusion <a name="conclusion"></a>

## This post <a name="this_post"></a>

Binary is the number system that all modern computers are based on. It uses 1s and 0s to represent numbers, and is used due to its simplicity and the robustness it provides when implementing digital circuitry (think of the signal & transistors). When using binary inside a computer we use encoding schemes to represent different kinds of data - two examples mentioned were character encoding and RGB encoding. We learned that binary is a base-2 number system and how this representation corresponds to denary/base-10, we also learned how to convert from denary into binary.

## Next post <a name="next_post"></a>

Another reason that we use binary is that it facilitates the use of something called *Boolean algebra*, sometimes called Boolean logic. Boolean algebra is the area of algebra in which the values of the variables can only take the discrete values of true or false, this corresponds to the 1s and 0s of a binary number. All modern computers operate according to the foundations laid down by Boolean algebra, and by using Boolean algebra we can reason about the behavior of the small digital circuits that combine to make up the complex microchips that we call CPUs. We can combine transistors to implement small circuits called logic gates, that we can use to build all kinds of complex integrated circuits such as CPUs.

If you haven't guessed the topic of the next post is Boolean algebra & logic gates.

Thanks for checking out the blog,

Max Sargent

[ibm-link]: https://www.ibm.com/support/knowledgecenter/en/SSLTBW_2.3.0/com.ibm.zos.v2r3.ioaq100/ascii_table_appendix.htm
[wiki-link]: https://simple.wikipedia.org/wiki/Transistor