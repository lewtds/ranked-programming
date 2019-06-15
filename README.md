# Ranked Programming

This repository contains the `ranked-programming` package for use with the [Racket](https://racket-lang.org) programming language. It is an implementation of the approach described in the following paper:

[Ranked Programming (Tjitze Rienstra)](https://github.com/tjitze/ranked-programming/blob/master/documentation/ranked_programming.pdf) (To be presented at IJCAI 2019).

Ranked programming is similar to probabilistic programming, except that the underlying uncertainty formalism is replaced with ranking theory, which measures uncertainty using degrees of surprise on the integer scale from 0 to infinity. Like probabilistic programming, ranked programming provides a simple and flexible way to represent models with uncertain behaviour, and to perform inference with such models. However, instead of using probabilities, we just specify what happens "normally" and what happens "exceptionally". For a more detailed description of this approach please read the aforementioned paper.

A complete reference for the ranked-programming package can be found [here](http://docs.racket-lang.org/ranked-programming@ranked-programming/index.html).

In this document we provide some instructions to get started with ranked programming in Racket. For a more general introduction to Racket please consult [Racket's own getting started](https://docs.racket-lang.org/getting-started/) guide.

# Getting Started

## Install Racket

The ranked programming library is written for use with the *Racket* programming language, which is based on the Scheme dialect of LISP. To get started, we first need to download and install Racket, which includes an editor called *DrRacket*. The download can be obtained [here](https://download.racket-lang.org).

## Install the Ranked Programming Package

The ranked programming library is distributed as a package and can be installed through DrRacket's package manager. To do so, open the DrRacket editor, open the *File* dropdown menu, and select *Package Manager*. In the Package Manager window, select the *Available from Catalog* tab, and click *Update Package List*. Then find and select the package called *ranked-programming* and click *Install*. 

<img src="https://github.com/tjitze/ranked-programming/blob/master/documentation/images/install_1.jpeg" width="600">

When done we can close the package manager window.

## Defining Your First Program

The DrRacket window has two text panels: the definitions panel (top half) and the interactions panel (bottom half). The purpose of the definitions panel is to define your program. Let's give a simple example. Any program starts by specifying its language. We use the Racket language, so we say `#lang racket`. In addition, we must say that we require the package called ranked-programming: `(require ranked-programming)`. We can then define our program. When we click *Run*, the output of our program is displayed in the interactions panel.

<img src="https://github.com/tjitze/ranked-programming/blob/master/documentation/images/program_1.jpeg" width="500">

Note that the syntax used here differs from the syntax of the language described in the paper. See the [reference](http://docs.racket-lang.org/ranked-programming@ranked-programming/index.html) for details.

## Interactive Evaluation of Expressions

Apart from displaying the output of a program, the interactions panel can be used to evaluate expressions interactively. This is useful for debugging purposes. It's also useful if we just want to experiment with the language. We can use the program we entered above as a starting point. Click *Run* and enter an expression (for example `(pr (nrm/exc "A" "B"))`) in the interactions panel.

<img src="https://github.com/tjitze/ranked-programming/blob/master/documentation/images/program_2.jpeg" width="500">

Furthermore, all the definitions of our program are available when evaluating expressions in the interaction panel. In the example below we interactively enter an expression which calls `(count 1)` and observes that the output is greater than 100.

<img src="https://github.com/tjitze/ranked-programming/blob/master/documentation/images/program_3.jpeg" width="500">

## Running examples

(TODO)
