---
title: My Design Studies
author: Alexandru Bolboacă
layout: post
---

I started a few years ago a few small projects to explore various ideas related to software design. I wanted to learn about functional programming in various languages, about property based testing, or about alternatives to microservices.

After a while, I realized that these projects can fall under the category of Design Studies: a type of deliberate practice used to discover how code can be structured in different ways depending on the design qualities that you seek to optimize.

Here is a short list:

## Pacman

I started this as an exploration of immutability and pure functions in groovy. It turned into property-based testing after refactoring from example based tests to data driven tests and finally to properties. Spock, the testing library for groovy, helped me a lot due to how seamless it is to introduce generators. 

I then wrote a version in C++ to compare the two solutions, and to see the C++ support for functional programming. Turns out, you need to think about memory allocation in the C++ solution - who would've thought about that! :)

Anyway, here's the groovy solution: [https://github.com/alexboly/pacmanKataPropertyBasedGroovy](https://github.com/alexboly/pacmanKataPropertyBasedGroovy) and the C++ solution: [https://github.com/alexboly/pacmanCpp](https://github.com/alexboly/pacmanCpp).

## Composability

How far can you take function composition in your language? I asked this question about groovy. The answer for groovy is pretty far; there's even a syntax construct for composing two functions:

~~~~{.java}
def composedFunction = firstFunction << secondFunction 
// composedFunction(params) is the same as firstFunction(secondFunction(params))
~~~~

The only thing I don't like is the curry method; I'd prefer a named parameter to make things clearer:

~~~~{.java}
def hasFirstName = { firstName, namedEntity ->
	namedEntity.firstName == firstName
}

def hasFirstNameAlin = hasFirstName.curry("Alin")
~~~~

Find the full example here: [https://github.com/alexboly/composabilityDesignStudy](https://github.com/alexboly/composabilityDesignStudy)


## Church encoding

[Church encoding](https://en.wikipedia.org/wiki/Church_encoding) is an interesting test for the functional programming support for your language. It's a way to write the types as functions; it has little practical use, but it is an interesting curiosity nonetheless.

I was curious about the C++ support for functional programming, so what better test? Turns out it's surprisingly good - other than the weird syntax. Here's the result: [https://github.com/alexboly/ChurchEncodingCpp](https://github.com/alexboly/ChurchEncodingCpp).

## Microservices or processes?

My first thought when hearing about microservices has been: this is another iteration of UNIX processes. Also, services are just an optimization of normal processes. So why wouldn't we use simple programs instead of services?

The thought evolved into an even more interesting idea. We are used to write tests as separate configuration, and I think this is due to historical reasons. It makes a lot of sense to have processes that can self test. So how about this?

Turns out self configure, self cleanup and self test are fairly easy to implement. There are a few challenges with self testing, especially figuring out how to avoid clashes with production data. The biggest challenge seems to be the interprocess communication - it's much nicer to communicate through REST / JSON / HTTP than through pipes. But there are always solutions to this problem.

This is still a work in progress, but a very interesting idea nonetheless. See the example here: [https://github.com/MozaicWorks/SelfContainedProcessesAsMicroservicesDesignStudy](https://github.com/MozaicWorks/SelfContainedProcessesAsMicroservicesDesignStudy).

## Other ideas

I did some more design studies, that I can't find right now. One was about an internal DSL in groovy called "cat" because instead of print it uses "meaow". 

I've also built in the past a small NoSQL database engine optimized for reading - structured in columns instead of lines, and parsers for specific XML files using a separate semantic and one-pass syntactic parser.

## Interesting?

Great to hear - how about telling me what you find useful or interesting through a tweet (see tweet handle below)?
