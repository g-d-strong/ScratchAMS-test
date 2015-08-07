
This exercise is based on the "Supermarket Checkout" kata by Dave Thomas (@PragDave).

Introduction
==========

For our workshop on Saturday we want to use a small programming exercise to focus some of the later discussion. You can use any programming language you like for this, of course. When you complete the sign-up form please tell us what language that you would prefer to use (we would like to get a mix of groups, some using Scratch and some using text-based programming languages like Python).

Since the the coding session will be quite short we suggest you think about the problem (below) beforehand. You might want to pay special care to think about how you might _share_ your code. We have made a github repository where you can upload your solutions, could you use that? Might you be able to share some _test_ code so that you can be sure the pieces of the solution that each person is contributing work properly together? These are typical questions that programmers have to have answers to when they work on code together.

Sharing
======


We will ask everyone to upload their solutions (as much as you get done, anyway) to github (don't worry if you don't have any experience with this, it's not essential). We have a public repository at <https://github.com/g-d-strong/ScratchAMS-test.git> that you can use. We suggest making a sub-directory for your team  (we'll give you a team number you can use).

The programming exercise
=====================

Our goal is to implement part of a supermarket checkout system. We won't be concerned with any of the screens the user sees, just the part that calculates the total bill when it sees the list of products the customer is buying.

Our program has to take a sequence of products and calculate a running total of the customers bill. Shops usually use unique identification numbers (called Stock Keeping Units - SKU's) for their products, but to keep this exercise simple we'll just use letters. Because prices change frequently our program needs to read a file of prices every time we start a new transaction. There is a sample file of prices in the github, or you can generate your own (for this exercise we are not very worried about where they come from. The challenge is just to calculate the total bill correctly).

Supermarket prices are not as simple as they first look. For this exercise we'll only include "multi-buy" prices: sometimes when you buy several of a particular item you get a special price. For example, bananas might be €1.99 per pack, but if buy 2 packs then you get them for a total of €3.00.

The price rules are described in a text file which has one rule per line: first the letter for the SKU, then a space, and then the price. There will only be one rule per line. Multi-buy rules appear when there is more than one letter on the line. Here is an example set of rules:

```
A 1.29
B 1.99
C 4.32
D 0.12
BB 3.00
AB 2.64
```

(that last rule might be advertised as "buy a bag of Apples, get your Bananas half price").

A few things to consider.

* The customer will, of course, swipe their purchases in whatever order they come out of the basket so your program can't assume that all the multibuy products will come together.
* If you want a bonus challenge, try to calculate a running total of the bill for the customer. Once you are doing this it should also be easy to tell the customer their total saving from multi-buys when they get to the end of the transaction.

