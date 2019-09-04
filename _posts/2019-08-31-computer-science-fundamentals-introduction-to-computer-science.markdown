---
layout: post
title: "CS Fundamentals I: Introduction to Computer Science"
date: 2019-08-31
description: Introducing Computer Science as a topic, and the fundamentals series. # Add post description (optional)
img: cs-fundamentals/introduction-to-computer-science/postimage.jpg # Add image post (optional)
---
Hi!

This post is the first in a series entitled *CS Fundamentals*. This series will touch on some key topics that are fundamental to building a understanding of computer science, and hopefully in a way which is easy to understand for someone who is completely new to the topic.

Todays post is an introduction into the discipline itself and will aim to answer these questions:

- [What is computer science?](#what_is_cs)
- [What does a computer scientist do?](#what_does_cs)
- [What is a computer?](#what_is_computer)
- [What is a computer program?](#what_is_program)

After answering these questions hopefully someone who has no idea about the subject might have a vague idea of what it is and why it is so fascinating.

# What is computer science? <a name="what_is_cs"></a>

The definition of computer science from google search is:

"*The study of the principles and use of computers.*" 

This definition is inaccurate, as it assumes that computers are required to study computer science. However computer science had been studied extensively prior to the invention of the computers that we are so familiar with today. In fact problems in computer science were tackled for decades using just a pencil and paper, this is because the roots of computer science lie in applied mathematics.

So if computer science is not the study of the principles and use of computers then what is it? I like to think of computer science as the study of information processing. After all a computer is just an information processing machine. [This][boston-university-link] definition from Boston University is my favorite:

"*Computer Science is the systematic study of the feasibility, structure, expression, and mechanization of the methodical processes that underlie the acquisition, representation, processing, storage, communication of, and
access to information.*"

Computer science is an extremely far-ranging field which overlaps with almost every other scientific discipline, this is because of how ubiquitous computers have become, there is no scientific field which does not benefit from the information processing power that modern computers provide. Below I have drawn a diagram (incomplete mind) that show some of the different areas of study that exist within computer science.

![Sub-fields diagram](/assets/img/cs-fundamentals/introduction-to-computer-science/sub-fields.jpg)

# What does a computer scientist do? <a name="what_does_cs"></a>

Following on from our definition of computer science, we now must define a computer scientist. Obviously a computer scientist is someone who studies computer science! However to answer this question I find that looking at vocations of computer scientists helps paints a better picture of what they do. By understanding what jobs computer scientists work, and also analyzing the typical traits that make for good workers within these jobs, we can understand what a computer scientist does on a day to day basis.

Looking at [this][balance-careers-link] article by thebalancecareers we can see some typical computer science careers:

- Computer and Information Systems Manager
- Computer Systems Analyst
- Computer Hardware Engineer
- Computer Programmer
- Computer Support Specialists
- Software Developer
- Web Developer

All these vocations are distinct, however what underpins each role is an understanding of computer science. These roles will all require a degree level understanding of computer science. If all the roles are distinct, but they require the same degree, then it must be the traits and skills the degree provides which connects them. According to [chron][chron-link] these include: 

- Deductive reasoning
- Information ordering
- Critical thinking
- Complex problem solving
- Programming
- Analytical thinking
- Active listening
- Learning

In short, a computer scientist is someone who has studied computer science, and therefore acquired a large amount of knowledge on the subject. They also excel at analyzing and creating solutions to complex problems, through the application of deductive reasoning and critical thinking.

Computer scientists typically work on the theoretical side of the field, as opposed to computer engineers who work on the hardware. However the fields of course overlap.

# What is a computer? <a name="what_is_computer"></a>

So now we have an understanding of computer science and what it really is, as well as what makes a (good) computer scientist. What about computers themselves? If we said earlier that computer science doesn't require computers, then what is a computer? 

The every day person considers a computer to be a laptop or desktop PC. But a computer scientist considers a computer to be an information processing device. Every part of our waking lives is filled with computers in this modern world. Your phone, TV, dishwasher, microwave, washing machine, car, blue-tooth headphones etc all contain computers. Although all these devices are different, the way that the underlying computers work is the same. Computer scientists call this concept the *stored program computer*.

To keep this as simple as possible for the purpose of this introductory article we will consider the stored program computer as depicted in the diagram below:

![Stored program computer diagram](/assets/img/cs-fundamentals/introduction-to-computer-science/storedprogramcomputer.jpg)

- CPU - Central processing unit, this is the part of the computer which carries out instructions.
- Memory - This part of the computer holds the instructions, and the data on which the instructions will operate.

The computer is essentially a machine which carries out a set of instructions on a given piece of data. The addresses arrow signifies the CPU requesting either the next instruction, or a piece of data. Every instruction or piece of data has an address within memory. This corresponds nicely with our idea of a computer as an information processing machine. 


# What is a computer program? <a name="what_is_program"></a>

We now know a computer is a machine which operates on data, by following a set of instructions. A computer program is the name we give to the set of instructions the computer is following. When a computer is following a set of instructions we say that the computer is executing the program. Computer programs are written by computer programmers, which is often a vocation where computer scientists work. However computers do not understand human language, human language is ambiguous by nature with many complexities and nuances. Computer programs are written in special languages called programming languages. These languages are extremely varied and the differences between them is an article in of itself.

When a program is written in a programming language, the code is known as source code.

The key idea to understand about computer programs and programming languages is that a computer only understands one language - binary. Binary representation is at the very heart of how modern computers work. For now understand that any computer program that is written in any programming language, i.e it is source code, must go through a process to be converted into binary. This process is called compilation, and the binary equivalent of source code is known as machine code.

![Compilation](/assets/img/cs-fundamentals/introduction-to-computer-science/compilation.jpg)

# Conclusion

To sum up what we have covered in this post we will answer the questions we asked at the start:

**What is computer science?**

Computer science is the study of information processing, not just the study of computers. It is a wide and varied field which overlaps many other scientific disciplines.

**What does a computer scientist do?**

A computer scientist solves problems, most computer scientists do this by writing computer programs.

**What is a computer?**

Computers are information processing machines, and they are ubiquitous - not just your laptop or desktop PC! Modern computers are stored program computers.

**What is a computer program?**

A computer program is a set of instructions for a computer to execute, it is written in a programming language (source code) and then compiled into binary (machine code).


In the next part of the CS Fundamentals series we will cover the topic of the binary number system.

Thanks for checking out the blog,

Max Sargent

[boston-university-link]: https://www.cs.bu.edu/AboutCS/WhatIsCS.pdf
[balance-careers-link]: https://www.thebalancecareers.com/computer-science-careers-525880
[chron-link]: https://work.chron.com/characteristics-computer-science-career-15434.html
