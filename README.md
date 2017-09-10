# sable
**Sable**, a Swift 4.0 - compliant implementation of the language targeting the JVM.

The Sable project is aimed to implement the Sable language - a Swift 4.0 - compliant language for the JVM (Java Virtual Machine). "Sable" is a transcription of *S-Able*, wich in turn stands for *Swift - Able*.

Sable is a hobbyist project and no person taking part in it is being paid for it. The Sable project is open source and is not funded by any company or public entity.

## Goals ('what')

The goals are:

**1) Develop a JVM toolset for Sable development.**

Such a toolset shall allow for full-cycle and full-range development targeting the JVM platform and its satellite- or supported technologies, just as it happens for most of JVM-compliant languages. A minimum toolset shall include:
   1- A compiler of Sable sources into JVM bytecode.
   2- A debugger.
   3- An Eclipse-based IDE, including the typical development supporting widgets (a smart editor, outline views, etc).

**2) Keeping Sable fully compliant with the Swift 4.0 specification, within the limits that the nature of the JVM imposes.**

Much of the Swift 4.0 programming paradigm, such as modules, classes, variables, functions, statements and other typical OOP concepts map more or less naturally into their JVM counterparts. In such cases, an equivalence mapping is to be applied between Swift and the JVM in order to implement Sable.

Nevertheless, Swift 4.0 does include certain concepts and language constructs aimed at low-level development, such as memory management facilities, that may difficult or pointless to implement in a JVM-based language. In such cases, the following approach shall be followed:
   1- If such a non-JVM construct can be implemented in the JVM without compromising any more prioritary goal than this one, then they shall be implemented.
   2- If such a non-JVM construct can be simulated in the JVM without compromising any more prioritary goal than this one, then they shall be simulated. "Simulating" a non-JVM construct is to be understood as offering an API fully implemented in the JVM that will offer an user of the non-JVM construct an equivalent semantic model to the one dictated by the Swift 4.0 specification.


## Goals ('how')

The main non-functional goals of the project (the HOW), which can be understood as aimed traits of the Sable implementation, are:

**1) Correctness.**

At the top of priorities is providing a correct implementation of the Swift 4.0 language that will behave in a correct way. "Correct" means not only compliant to the specification, but also bug-free (to a realistic degree). We want to offer a product that people can rely on and trust.

Formal methods of sofware design and/or verification, including formal semantics, should be applied wherever feasible. Formal methods, if aplied correctly, can give critical parts of software artifacts the reliability of a mathematically proven model. Exhaustive testing will be required but only as a second option to formal methods, wherever the latter are not feasible or confortable to apply.

**3) Ergonomy.**

This is a goal than cannot be stressed enough. Sable and its toolset should be easy to use, but moreover - nice to use. They should allow the end-user to develop in a natural, confortable and high-productive way. Therefore an user-oriented approach, keeping in mind the user's mind, his needs and other state-of-the-art solutions in every case shall guide every feature design and implementation.

The software market has offered and still produces plenty of both successful unsuccessful user-interaction solutions. Following the old good principle of not attempting to reinvent the wheel (but using the wheel to invent something new), the Sable project will follow two documents as a guide to design user interaction mechanisms: Apple User Interface Guidelines and Eclipse user interface guidelines. Read below to know more about them.

**4) Simplicity.**

Simplicity means not doing more than it's necessary. We want to keep both the product and the source code simple and easily usable, preferring minimalistic, proven solutions, both in the internal architecture of Sable and in its interface with the end-user.


## Non-Goals

We are  developing Sable in our spare time within a non-profit initiative and, if asked to make things good, fast and many, we can at most choose two of them ;) Therefore we are forced to state the *NON-GOALS* of the project. A characteristic being a *non-goal* does not mean that Sable cannot or will not possess it; it just means that the Sable team will not dedicate any time nor effort to them if that compromises any of the GOALS stated above.

1) Performance (understood as execution time of either Sable programs or of the Sable toolset).
2) Offering JVM "native" support for non-Swift, but commonly used with Swift artifacts or technologies (Foundation, Cocoa, etc).
3) Staying extremely up-to-date with the latest changes in the Swift standard.


## Team work and collaboration

The guy writing these lines is not going to make this happen on his own alone (at least not in the forseeable future for this universe). Therefore every help and contribution is welcome.

For the above goals to have a chance to be realized, my experience tells me that a very bare minimum set of collaboration rules are necessary, so that contributions (for example with source code and artifacts) fit the project's goals and help them. The following is one I've just come up with:

1. There is a team of *guiding developers* that ultimately have to decide whether a proposal of a contribution or a contribution itself can be accepted. If it does not get accepted, the guiding developers shall suggest the contributor either a way to fix the proposal/contribution, or a clear explanation of the objective reasons for which the proposal/contribution is to be rejected.

The *guiding developers* team also decides whether to enlarge the team with new members.

2. For the beginning, the only member in the *guiding developers* team is the guy writing these lines, David. If only because there ir no other around. However, I look forward to add new members!

3. Architecture and coding of features should be done in accordance with the so-called clean-code principles. In general, good software engineering is required. **We are not here to be ridiculous**.

For the time being, this PDF should serve as a guide for coding guidelines, until the team of *guiding developers* comes up with the official Sable source code guidelines:

https://www.planetgeek.ch/wp-content/uploads/2013/06/Clean-Code-V2.2.pdf

4. User interface design rules are just so much, or even more important than coding rules, according to the project's goals. The following documents shall be used as a guide for designing user interaction solutions (e.g. in the IDE or the compiler command line), in the cases where they are not contrary to the Sable project's goals:

https://developer.apple.com/macos/human-interface-guidelines

5. The *guiding developers* team may change the rules for team collaboration and work if there are good reasons for it (i.e if those resons serve the project's goals).

## What now? What next?

If you have been keeping reading up to this point, I am happy to tell you that have already contributed to the Sable project! :) But if you want to take it a step further, you could:

1) Think about contributing as developer
2) Tell other people about the Sable project and that developers are welcome

By the time being, not much is done. A grammar an Antlr4 parser is being defined and I am doing some Java low-level libraries that can be used for low-level support in Swift. I am also thinking over certain architecture issues, such as how to implement so-called Swift "builtins" and IR intrinsic functions in the JVM. I will be publishing docs and new things as I have them ready.

See you at the Sable project!


Cheers!

David Guardado Barcia



