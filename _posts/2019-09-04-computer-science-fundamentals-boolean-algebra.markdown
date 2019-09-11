---
layout: post
title: "CS Fundamentals III: Boolean Algebra & Logic Gates"
date: 2019-09-04
description: Basics of boolean algebra and logic gates. # Add post description (optional)
img:  cs-fundamentals/boolean-algebra-and-logic-gates/postimage.jpg # Add image post (optional)
---

Hi!

This post is the third in the CS Fundamentals series, todays topic is another idea critical to the inner workings of all modern computer systems - *Boolean algebra*. Boolean algebra is similar to the algebra we all learned in maths at school, but the variables (X,Y,Z etc) can only take two values - true or false. In the "regular" algebra that we learned at school these variables could take the value of any number.

---

# Contents
1. [What is boolean algebra?](#what_is_boolean_algebra)
2. [What is a logic gate?](#what_is_logic_gate)
3. [Boolean operators & equivalent logic gates](#boolean_operators_and_gates)
	1. [Basic operators](#basic)
		1. [AND](#and)
		2. [OR](#or)
		3. [NOT](#not)
	2. [Combined operators](#combined)
		1. [XOR](#xor)
		2. [NAND](#nand)
		3. [NOR](#nor)
	3. [Cheat-sheet](#cheatsheet)
	4. [Simple example](#simple-example)
4. [Boolean algebra laws](#laws)
	1. [Commutativity](#commutativity)
	2. [Identity](#identity)
	3. [Complement](#complement)
	4. [Idempotent](#idempotent)
	5. [Double negation](#double_negation)
	6. [Associativity](#associativity)
	7. [Distributivity](#distributivity)
	8. [de Morgans'](#de_morgans)
5. [Boolean algebra expressions](#expressions)
	1. [Question 1](#q1)
	2. [Question 2](#q2)
	3. [Question 3](#q3)
6. [Conclusion](#conclusion)
	1. [This post](#this)
	2. [Next post](#next)

---

# What is Boolean algebra? <a name="what_is_boolean_algebra"></a>

Boolean algebra is a part of an area of maths known as *discrete mathematics*, this area of maths deals with discrete variables opposed to continuous variables. If a variable is discrete it can only take a value from a set of values, if a variable is continuous is can take on any value. The algebra we all think of when we hear the word algebra operates using continuous variables.

To put it simply:

- Boolean algebra - X,Y,Z can only be **TRUE** or **FALSE** (this corresponds to the 1 and 0 of binary).
- Regular algebra - X,Y,Z can be any  number.

Also on top of this Boolean algebra has its own set of operators, it doesn't use + - / \*. It uses **AND**, **OR** and **NOT** operators.

![AND Truth Table](/assets/img/cs-fundamentals/boolean-algebra-and-logic-gates/boolean_algebras.jpg){: .center-image}

If you've noticed the capitalization of the word Boolean that is because Boolean algebra was first introduced in 1847 by a mathematician named George Boole, over the following years the idea was refined and perfected by various other mathematicians. 

Boolean algebra dictates the rules by which we can build circuits. This link was first fully realized in the 1930's by Claude Elwood Shannon, a well known mathematician and electronic engineer. In his masters thesis he showed that electronic circuits made up of switches (think back to the previous article and how transistors that make up CPUs are tiny electronic switches) could solve all problems that Boolean algebra could solve. He showed this through the use of an abstraction called a *logic gate*.

---

# What is a logic gate? <a name="what_is_logic_gate"></a>

A logic gate is simply a device which implements a Boolean operator. This is how Claude Elwood Shannon combined the theoretical area of maths known as Boolean algebra with the physical reality of electronic circuitry - a logic gate can be made up of electrical switches or it can be entirely theoretical. It is just a way of modeling the complexities of Boolean algebra in such a way that it can be translated into the real world, and therefore be used to create real circuits.

A logic gate takes in inputs that are either **TRUE** or **FALSE**, and outputs a value either **TRUE** or **FALSE**. In a computer this would be 1 or 0, and in a circuit this would be voltage **ON** or **OFF**. Can you start to see how all these things are working together?

![Equivalent Representations](/assets/img/cs-fundamentals/boolean-algebra-and-logic-gates/equivalent.jpg){: .center-image}

We can represent anything in a computer system using binary, we can create circuits that can manipulate these representations through the use of logic gates, and the logic gates themselves are a manifestation of Boolean algebra - the algebra of discrete variables. The 1 and 0 of binary are the discrete variables!

Interesting fact - Leibniz (the other inventor of calculus) studied the binary number system over 100 years before Boole came up with Boolean algebra, and he predicted its use in combining arithmetic and logic in the way that modern computers do. He was a genius who started university at 14 and graduated at 16.

---

# Boolean operators & equivalent logic gates <a name="boolean_operators_and_gates"></a>

So we know now that Boolean algebra is the algebra of two discrete values, typically written as **TRUE** and **FALSE**. We also know that the operators in this algebra are **AND**, **OR** and **NOT**. Furthermore we know that a logic gate is just a  representation of these operators, this allows for the creation of electronic circuits that follow the rules of Boolean algebra. Lets look at the basic operators and their equivalent logic gates.

## Basic operators <a name="basic"></a>

We can describe the operators in several different ways. I will first write what the operator does and then show how we can write it in a statement. Then we will derive a truth table. Finally we will look at the shape of its equivalent logic gate and how you would write it in using proper mathematical notation.

### AND <a name="and"></a>

The **AND** operator will return **TRUE** if and only if both of the input values are also **TRUE**. 

Consider the statement:

> "If I have money **AND** I have handed in my coursework, then I will go for a pint." 

We can represent this statement in Boolean algebra by assigning variables:

- x - Do I have money or not?
- y - Have I handed in my coursework?
- z - Will I go for a pint?

Then the entire statement is:

> x **AND** y = z

Now lets look at the value of the statement z given each variable, given that we know both must be **TRUE** to provide a **TRUE** result.

- x = **FALSE** y = **FALSE** - I have no money, I haven't handed in my coursework, I'm not going for a pint. 
- x = **FALSE** y = **TRUE** - I have no money, I have handed in my coursework, I'm not going for a pint.
- x = **TRUE** y = **FALSE** - I have money, I haven't handed in my coursework, I'm not going for a pint.
- x = **TRUE** y = **TRUE** - I have money, I have handed in my coursework, I'm going for a pint. - The ideal scenario.

This is the essence of a truth table. It shows you the truth value of the output, in this case z, given the truth values of the inputs. Check the truth table for the **AND** operator:

![AND Truth Table](/assets/img/cs-fundamentals/boolean-algebra-and-logic-gates/and_table.jpg){: .center-image}

When we represent the **AND** operator as a logic gate we draw it like this:

![AND Gate](/assets/img/cs-fundamentals/boolean-algebra-and-logic-gates/and_gate.jpg){: .center-image}

When we use the **AND** operator in an algebraic expression it can be written like this:

![AND Expression](/assets/img/cs-fundamentals/boolean-algebra-and-logic-gates/and_expr.jpg){: .center-image}

### OR <a name="or"></a>

The **OR** operator will return **TRUE** if any input is **TRUE**.

Consider the statement:

> "If I have money **OR** I have handed in my coursework, then I will go for a pint."

We can use the same representations of our variables as we did for the **AND** operator.

Then the entire statement is:

> x **OR** y = z

Lets work through the statement in the same way, given that we know only one variable needs to be **TRUE** to provide a **TRUE** result.

- x = **FALSE** y = **FALSE** - I have no money, I haven't handed in my coursework, I'm not going for a pint. 
- x = **FALSE** y = **TRUE** - I have no money, I have handed in my coursework, I'm going for a pint.
- x = **TRUE** y = **FALSE** - I have money, I haven't handed in my coursework, I'm going for a pint.
- x = **TRUE** y = **TRUE** - I have money, I have handed in my coursework, I'm going for a pint. - The more realistic scenario.

Here is the truth table for the **OR** operator:

![OR Truth Table](/assets/img/cs-fundamentals/boolean-algebra-and-logic-gates/or_table.jpg){: .center-image}

When we represent the **OR** operator as a logic gate we draw it like this:

![OR Gate](/assets/img/cs-fundamentals/boolean-algebra-and-logic-gates/or_gate.jpg){: .center-image}

When we use the **OR** operator in an algebraic expression it can be written like this:

![OR Expression](/assets/img/cs-fundamentals/boolean-algebra-and-logic-gates/or_expr.jpg){: .center-image}

### NOT <a name="not"></a>

The **NOT** operator is slightly different from the previous gates. It only takes 1 input, and inverts it. This is why it is sometimes called an inverter or a negation.

Consider the statement:

> "I am going for a pint."

We can represent this single statement as a single variable x.

- If x is currently **TRUE**, then **NOT** x would be **FALSE**.
- If x is currently **FALSE**, then **NOT** x would be **TRUE**.

Here is the truth table for the **NOT** operator:

![NOT Truth Table](/assets/img/cs-fundamentals/boolean-algebra-and-logic-gates/not_table.jpg){: .center-image}

When we represent the **NOT** operator as a logic gate we draw it like this:

![NOT Gate](/assets/img/cs-fundamentals/boolean-algebra-and-logic-gates/not_gate.jpg){: .center-image}

When we use the **NOT** operator in an algebraic expression it can be written like this:

![NOT Expression](/assets/img/cs-fundamentals/boolean-algebra-and-logic-gates/not_expr.jpg){: .center-image}

## Combined operators <a name="combined"></a>

The three previous operators are the building blocks for everything else in Boolean algebra and we can combine them to do different things. There are a few common combinations of these three which are so common they get their own names.

### XOR <a name="xor"></a>

The **XOR** operator, also called **exclusive-OR**, will return **TRUE** if and only if exactly 1 input is **TRUE**.

Here is the truth table for the **XOR** operator:

![XOR Truth Table](/assets/img/cs-fundamentals/boolean-algebra-and-logic-gates/xor_table.jpg){: .center-image}

When we represent the **XOR** operator as a logic gate we draw it like this:

![XOR Gate](/assets/img/cs-fundamentals/boolean-algebra-and-logic-gates/xor_gate.jpg){: .center-image}

When we use the **XOR** operator in an algebraic expression it can be written like this:

![XOR Expression](/assets/img/cs-fundamentals/boolean-algebra-and-logic-gates/xor_expr.jpg){: .center-image}


### NAND <a name="nand"></a>

The **NAND** operator, also called **NOT-AND**, is the opposite of the **AND** gate.

Here is the truth table for the **NAND** operator:

![NAND Truth Table](/assets/img/cs-fundamentals/boolean-algebra-and-logic-gates/nand_table.jpg){: .center-image}

When we represent the **NAND** operator as a logic gate we draw it like this:

![NAND Gate](/assets/img/cs-fundamentals/boolean-algebra-and-logic-gates/nand_gate.jpg){: .center-image}

When we use the **NAND** operator in an algebraic expression it can be written like this:

![NAND Expression](/assets/img/cs-fundamentals/boolean-algebra-and-logic-gates/nand_expr.jpg){: .center-image}

### NOR <a name="nor"></a>

The **NOR** operator, also called **NOT-OR**, is the opposite of the **OR** gate.

Here is the truth table for the **NOR** operator:

![NOR Truth Table](/assets/img/cs-fundamentals/boolean-algebra-and-logic-gates/nor_table.jpg){: .center-image}

When we represent the **NOR** operator as a logic gate we draw it like this:

![NOR Gate](/assets/img/cs-fundamentals/boolean-algebra-and-logic-gates/nor_gate.jpg){: .center-image}

When we use the **NOR** operator in an algebraic expression it can be written like this:

![NOR Expression](/assets/img/cs-fundamentals/boolean-algebra-and-logic-gates/nor_expr.jpg){: .center-image}

## Cheat-sheet <a name="cheatsheet"></a>

As a reference here is all the information from the this section in one image:

![Gates Cheat-sheet](/assets/img/cs-fundamentals/boolean-algebra-and-logic-gates/gates-cheatsheet.jpg){: .center-image}

## Simple example <a name="simple-example"></a>

To test our understanding of what we have covered so far lets look at a simple combination of logic gates and calculate the output value for a given set of input values.

![Simple example 1](/assets/img/cs-fundamentals/boolean-algebra-and-logic-gates/simple_ex_1.jpg){: .center-image}

Using the input values of v = **TRUE** , w = **FALSE**, x = **FALSE**, y = **TRUE**.

- v . w = T . F = F
- x + y = F + T = T
- (v . w) + (x + y) = F + T = T
- z = T


---

# Boolean algebra laws <a name="laws"></a>

Hopefully we have now developed a rudimentary understanding of what Boolean algebra is, and how it relates to logic gates and circuits. Boolean algebra has several laws which helps us to manipulate algebraic expressions to more easily calculate the values of complex expressions. These might seem confusing at first, to really gain an understanding try constructing a truth table of the equivalent expressions.

## Commutativity <a name="commutativity"></a>

The law of commutativity states that the order of the terms for an expression can be changed and the end will result will be no different.

![Commutativity](/assets/img/cs-fundamentals/boolean-algebra-and-logic-gates/commutativity.jpg){: .center-image}

## Identity <a name="identity"></a>

The law of identity shows how expressions behave when one of the terms is fixed.

![Identity](/assets/img/cs-fundamentals/boolean-algebra-and-logic-gates/identity.jpg){: .center-image}

## Complement <a name="complement"></a>

The law of complement shows the relationship between a variable and its negation. For example a variable OR its negation will always be true and a variable AND its negation will always be false.

![Complement](/assets/img/cs-fundamentals/boolean-algebra-and-logic-gates/complement.jpg){: .center-image}

## Idempotent <a name="idempotent"></a>

The law of idempotent shows how an expression behaves when a variable is repeated. It can be simplified to itself.

![Idempotent](/assets/img/cs-fundamentals/boolean-algebra-and-logic-gates/idempotent.jpg){: .center-image}

## Double negation <a name="double_negation"></a>

The law of double negation shows that when a variable is negated twice then the negation is negated, effectively meaning the variable is just equal to itself.

![Double Negation](/assets/img/cs-fundamentals/boolean-algebra-and-logic-gates/double_negation.jpg){: .center-image}

## Associativity <a name="associativity"></a>

The law of associativity shows the different ways that like terms can be grouped together and the end result remain the same.

![Associativity](/assets/img/cs-fundamentals/boolean-algebra-and-logic-gates/associativity.jpg){: .center-image}

## Distributivity <a name="distributivity"></a>

The law of distributivity is similar to bracket expansion in traditional multiplication. See how the outer expression is effectively applied to the variables in the brackets, the operator in the brackets becomes the operator between the new sets of two brackets.

![Distributivity](/assets/img/cs-fundamentals/boolean-algebra-and-logic-gates/distributivity.jpg){: .center-image}

## de Morgans'<a name="de_morgans"></a>

de Morgans' law is a special law that shows how AND and OR can be made to be equivalent through the use of the negation operator. This idea will be covered in more technical posts about propositional logic, in propositional logic AND and OR are called conjunction and injunction respectively. Essentially we can change an AND to an OR or vice-versa through the manipulation of negation operations.

![de Morgans'](/assets/img/cs-fundamentals/boolean-algebra-and-logic-gates/demorgans.jpg){: .center-image}

---

# Questions <a name="questions"></a>

Now we know as much about Boolean algebra as we need to look at more complex examples. We can take a Boolean expression and create a logic gate diagram, take a truth table and fill it out, or take a logic gate diagram and create a truth table. All these things are interchangeable ways of understanding the abstract concept of Boolean algebra.

## Question 1 <a name="q1"></a>

Given the Boolean expression below, construct a logic gate diagram and determine the output when inputs equal to x = FALSE, y = TRUE by constructing a truth table.

![Question 1](/assets/img/cs-fundamentals/boolean-algebra-and-logic-gates/q1.jpg){: .center-image}

<details>
<summary>
Click for answer.
</summary>
<p>

<img src="/assets/img/cs-fundamentals/boolean-algebra-and-logic-gates/a1.jpg" alt="Answer 1'">
 Does this truth table look familiar? It is the XOR operation. This is one way that XOR can be constructed from the basic operators!
</p>
</details>

## Question 2 <a name="q2"></a>

Given the logic gate diagram, work out the corresponding Boolean expression and simplify.

![Question 2](/assets/img/cs-fundamentals/boolean-algebra-and-logic-gates/q2.jpg){: .center-image}

<details>
<summary>
Click for answer.
</summary>
<p>

<img src="/assets/img/cs-fundamentals/boolean-algebra-and-logic-gates/a2.jpg" alt="Answer 2'">

</p>
</details>

## Question 3 <a name="q3"></a>

Complete the given truth table, then draw the logic gate diagram.

![Question 3](/assets/img/cs-fundamentals/boolean-algebra-and-logic-gates/q3.jpg){: .center-image}

<details>
<summary>
Click for answer.
</summary>
<p>

<img src="/assets/img/cs-fundamentals/boolean-algebra-and-logic-gates/a3.jpg" alt="Answer 3'">

</p>
</details>

---

# Conclusion <a name="conclusion"></a>

## This post <a name="this"></a>

Let's summarize what we have covered in this post as it is much more abstract and technical then the previous posts in this series.

- We learned that Boolean algebra is a type of algebra that uses discrete variables (TRUE, FALSE) and its own operators (AND, OR, NOT).
- We learned a logic gate is an abstraction that represents a Boolean operation, it can be used abstractly in diagrams or be physically implemented using switches (such as transistors)
- We learned how each basic operator works, its truth table, its logic gate symbol and its algebraic notation
- We learned about combined operators that can be made from AND, OR, NOT operators
- We learned about several "Laws of Boolean algebra" which allow us to manipulate and simplify Boolean algebra, this can help us reduce the size of circuits to the minimum required number of logic gates
- We practiced three difficult questions

A lot to take in for one post, but understanding Boolean algebra is fundamental to understanding computer science!

## Next post <a name="next"></a>

The next post will be a change of track from the binary and Boolean algebra that we have been studying. We will look at a more complex version of Computer Architecture than the stored program computer mentioned in the first post.

Thanks for checking out the blog,

Max Sargent