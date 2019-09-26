---
layout: post
title: "CS Fundamentals IV: Computer Architecture"
date: 2019-09-04
description: Basics ofcomputer architecture. # Add post description (optional)
img:  cs-fundamentals/computer-architecture/postimage.jpg # Add image post (optional)
---

Hi!

This post is the fourth in the CS Fundamentals series, todays topic is a change in direction to the previous maths oriented posts on binary and boolean algebra. Today we will cover the topic of computer architecture! We will do so in a way which is tailored for readers new to the topic who have no idea about the different parts of a computer - so any techies don't be alarmed if you read something that you know to only be partly true. Sometimes it is useful to sacrifice complexity and detail to help people understand basic concepts, the details then come after a basic understanding is established.

I will take a holistic approach to this topic covering some hardware and software components of a computer system, as well as explaining what an instruction set is and how it acts as the interface between hardware and software.

---

# Contents
<!-- MarkdownTOC autolink="true" -->

- [Introduction](#introduction)
	- [Hardware Vs Software](#hardware-vs-software)
	- [High level view](#high-level-view)
- [Instruction Set Architecture](#instruction-set-architecture)
	- [What is an instruction set architecture?](#what-is-an-instruction-set-architecture)
	- [How does it interface with software?](#how-does-it-interface-with-software)
	- [How does it interface with hardware?](#how-does-it-interface-with-hardware)
- [Software](#software)
	- [High level view](#high-level-view-1)
	- [What is an assembler?](#what-is-an-assembler)
	- [What is a compiler?](#what-is-a-compiler)
	- [What is an operating system?](#what-is-an-operating-system)
	- [What is an application?](#what-is-an-application)
- [Hardware](#hardware)
	- [Von Neumann architecture](#von-neumann-architecture)
		- [What is the CPU?](#what-is-the-cpu)
		- [What is memory?](#what-is-memory)
		- [What are inputs?](#what-are-inputs)
		- [What are outputs?](#what-are-outputs)
- [Conclusion](#conclusion)

<!-- /MarkdownTOC -->

---

# Introduction

## Hardware Vs Software 

A computer system is made up of both software and hardware. Software is the term used for the collection of computer programs that the system is running, this includes everything from the device drivers running your speakers, web browser, operating system etc. Any code that is executed or stored on the computer is software.

Hardware is the term used for the physical devices that make up the computer. For PCs this includes the hardware of the computer itself such as CPU, memory, GFX cards, motherboards etc as well as the hardware of peripheral devices such as mice, keyboards, monitors and everything inbetween.

This applies to small computers such as microcontrollers just as much as desktop PCs. The hardware would include the microcontroller and any electronics that are attatched and the software is the firmware that is written onto the chip.


## High level view

Below is a simple diagram showing how the hardware and software are related in a computer system. As you can see there is something inbetween them which allows them to communicate in a standardized way - the instruction set architecture.

![High Level](/assets/img/cs-fundamentals/computer-architecture/high-level.jpg){: .center-image}

We will slowly build on this diagram until we have a better picture of the computer architecture as a whole.

---

# Instruction Set Architecture

## What is an instruction set architecture?

There must be something that facilitates the communication between the hardware and the software somehow. Cast your mind back to the introduction to computer science post where we talked about a computer as executing instructions stored in its memory and making changes to the data also stored in memory. How does the CPU know what instruction does what? This is the purpose of the instruction set architecture.

The instruction set architecture can be thought of as a virtual model of a computer. It is an interface between the hardware and the software, examples of an instruction set architecture are the x86 and x64 architectures. In computer science when we say interface we mean a shared boundary between two or more parts of a system where information is exchanged. This boundary is always well defined, it can be thought of as a contract which dictates the behaviour of the system at the boundary, this means that both sides of the system know what to expect.

When a CPU meets the criteria for an instruction set architecture we say that the CPU implements the architecture.

## How does it interface with software?

The instruction set architectures interface with the software is simple, each instruction that can be performed by a CPU that implements a given architecture has a mnemonic (set of letters to help in remembering for example: ADD could mean add and LDA could mean load) which corresponds to that instruction. This is what we call the instruction set. To help understand here is a snippet of the x86 instruction set from wikipedia:

![Mnemonics](/assets/img/cs-fundamentals/computer-architecture/mnemonic.jpg){: .center-image}

Each one of these mnemonics is paired with a binary number, when the CPU loads this number it will carry out the related instruction. Sometimes the instruction requires certain operands - additional variables, for example the ADD instruction will also require two numbers. This might not seem like a very complex interface, but it is from here that all computer programs are built. This instruction set lists all operations that can be carried out by a given CPU.

We will find out later how this simple instruction set can be built on to create more complex programming languages such as assembly language, C and eventually much higher level languages like Python.


## How does it interface with hardware?

To have an interface with the instruction set architecture the CPU must be designed to be able to execute all the instructions that are listed in the given architecture. This simple premise is what guarantees cross compatability between different CPU architectures. If Intel and AMD didnt follow an instruction set architecture then there would be no guarantee that software written on one would run on the other.

If a CPU implements the instruction set architecture, then it will be able to perform all the functionality defined in the interface. For example both AMD and Intel have processors which implement the x86 and x64 architectures, however how these CPUs and corresponding hardware work can be massively different under the hood. The key is as long as they implement the interface then whatever happens on the other side is irrelevant.

Just as a side note - when an instruction set architecture is actually implemented physically in a CPU this is called a microarchitecture. With AMD and Intel we would say they implement the same instruction set architecture but do it using different microarchitectures.

---

# Software

## High level view

## What is an assembler?

## What is a compiler?

## What is an operating system?

## What is an application?

---

# Hardware

## Von Neumann architecture

### What is the CPU?

### What is memory?

### What are inputs?

### What are outputs?

---

# Conclusion