> We are about to study the idea of a computational process. Computational processes are abstract beings that inhabit computers. As they evolve, processes manipulate other abstract things called data. The evolution of a process is directed by a pattern of rules called a program. People create programs to direct processes. In effect, we conjure the spirits of the computer with our spells. > > The programs we use to conjure processes are like a sorcerer's spells. They are carefully composed from symbolic expressions in arcane and esoteric programming languages that prescribe the tasks we want our processes to perform. > > A computational process, in a correctly working computer, executes programs precisely and accurately. Thus, like the sorcerer's apprentice, novice programmers must learn to understand and to anticipate the consequences of their conjuring. > > —Abelson and Sussman, SICP (1993)

>"The varied titles of Turing's published work disguise its unity of purpose. The central problem with which he started, and to which he constantly returned, is the extent and the limitations of mechanistic explanations of nature. All his work, except for three papers in pure mathematics ... grew naturally out of the technical problems encountered in these enquiries. His way of tackling the problem was not by philosophical discussion of general principles, but by mathematical proof of certain limited results: in the first instance the impossibility of the too sanguine programme for the complete mechanization of mathematics, and in his final work, the possibility of, at any rate, a partial explanation of the phenomena of organic growth by the blind" operation of chemical laws.


------------------------------------------------------------------------------------------------------------------------------


## What is Computer Science? 


> Knuth (1974b) said that CS is the study of algorithms and surrounding phenomena such as the computers that they run on. CS is the the study both of algorithms and of the computers that execute them. 


CS can have multiple definitions: 

    - natural science of procedure 
    - “artificial science” (as opposed to the “natural science”) of the phenomena surrounding computers
    - CS is the study of how to represent and process information and of the machines and systems that do this
    - said that it is a new kind of science (neither a physical, a biological, nor a social science) of natural and artificial information processes
    - Loui (1987) suggested that CS is a new kind of engineering that studies the theory, design, analysis, and implementation of information-processing algorithms
    - "CS is “a sort of spectrum . . . with ‘science’ on the one end and ‘engineering’ on the other” 

If we want to pick one then we can settle on the following: 

> CS is the scientific study of what problems can be solved, what tasks can be accomplished, and what features of the world can be understood “computationally”—that is, using the minimal language of a Turing Machine—and then to provide algorithms to show how this can be done efficiently, practically, physically, and ethically. 


## Theoratical Computer Science concerns itself with the following questions: 

0. What is computation? 
1. What can be computed, and how? 
2. What can be computed efficiently, and how? 
3. What can be computed practically, and how? 
4. What can be computed physically, and how? 
5. What can be computed ethically, and how?


## Great Ideas/Insights of CS: 

   - A (programmable) computer is a physically plausible implementation of anything logically equivalent to a universal Turing machine.

   - An automaton (plural: automata) is a mathematical model of a computing device.

   - Turing machines are an abstraction of computers with unbounded resources.

   - Finite automata are an abstraction of computers with finite resource constraints.
   
   - DFAs are the simplest type of automaton

### That “minimal language” can be described by four “great insights of CS”: 

1. The representational insight: Only two nouns are needed to express any algorithm. 


> All the information about any computable problem can be represented using only two nouns: ‘0’ and ‘1’

Up until that time [that is, the time of publication of Shannon’s “Mathematical
Theory of Communication” (Shannon, 1948)], everyone thought that communication was involved in trying to find ways of communicating written language, spoken language, pictures, video, and all of these different things— that all of these would require different ways of communicating. Claude said
no, you can turn all of them into binary digits. And then you can find ways
of communicating the binary digits. (Robert Gallager, quoted in Soni and
Goodman 2017)


2. The processing insight: Only three verbs are needed. 

3. The structural insight: Only three rules of grammar are needed. 

4. A “closure” insight: Nothing else is needed. This is the import of the ChurchTuring Computability Thesis that anything logically equivalent to a Turing Machine (or the lambda calculus, or recursive functions, or . . . ) suffices for computation.


And there is a fifth insight that links this abstract language to computers: 

5. The implementation insight: Algorithms can be carried out by physical devices
------------------------------------------------------------------------------------------------------------------------------

## Big-0 Notation


Big-0 Notation gives an upper bound of the complexity in the worst case, helping to quantify performance as the input size becomes arbitrarily large.


Let $f$ be a function that describes the running time of a particular algorithm for an input of size n:
$$
\begin{array}{c}
f(n)=7 \log (n)^{3}+15 n^{2}+2 n^{3}+8 \\
0(f(n))=0\left(n^{3}\right)
\end{array}
$$




------------------------------------------------------------------------------------------------------------------------------
## Problem Solving and Algorithms 

"Problem-Solving is a holistic blend of complex skills and finely tuned attitudes. It requires a balance of intutiion and formal rigour, of resilience and creativity. It depends too on collaboration and the ability to see out feedback and act on it. And so much more: certainly too for a single test to do justice.'


"In its purest form, mathematics is the perfect expression of human thought that marries logic with creative thought". 

"[The Euclidean algorithm] is the granddaddy of all algorithms, because it is the oldest nontrivial algorithm that has survived to the present day." - Donald Knuth, The Art of Computer Programming


Learning the art of solving new problems by mapping them to existing solved problems

"Reduction is a way of converting one problem to another problem in such a way that the solution to the second problem can be used to solve the first problem" - Theory-Of-Computation-Michael-Sipser

------------------------------------------------------------------------------------------------------------------------------


### Do I really understand the problem?
(a) What exactly does the input consist of?
(b) What exactly are the desired results or output?
(c) Can I construct an input example small enough to solve by hand?

### What happens when I try to solve it?
(d) How important is it to my application that I always find the optimalanswer? Can I settle for something close to the optimal answer?
(e) How large is a typical instance of my problem? Will I be working on10items? 1,000 items? 1,000,000 items?
(f) How important is speed in my application? Must the problem be solved within one second? One minute? One hour? One day?
(g) How much time and effort can I invest in implementation? Will I belimited to simple algorithms that can be coded up in a day, or do I have thefreedom to experiment with a couple of approaches and see which is best?
(h) Am I trying to solve a numerical problem? A graph algorithm problem? A geometric problem? A string problem? A set problem? Which formulation seems easiest?

### Can I find a simple algorithm or heuristic for my problem?

(a) Will brute force solve my problem correctly by searching through allsubsets or arrangements and picking the best one?
    i. If so, why am I sure that this algorithm always gives the correct answer?
    ii. How do I measure the quality of a solution once I construct it?
    iii. Doesthis simple, slow solution run in polynomial or exponential time? Is my problemsmall enough that this brute-force solution will suffice?
    iv. Am I certain that myproblem is sufficiently well defined to actually have a correct solution?
    
(b) Can I solve my problem by repeatedly trying some simple rule, likepicking the biggest item first? The smallest item first? A random item first? 
    i. If so, on what types of inputs does this heuristic work well? Do thesecor-respond to the data that might arise in my application? 
    ii. On what types of inputs does this heuristic work badly? If no suchexam-ples can be found, can I show that it always works well? 
    iii. How fast does my heuristic come up with an answer? Does it have a simple implementation?

other hacks 
    See Cracking the coding interview 


-----



#### What should we consider fundamental?

> A fair question, and a full answer would be too long for a comment (though it would fit in a blog post, which I'll go ahead and write now since this seems to be an issue). But I'll take a whack at the TL;DR version here.
> AI, ML, and NLP and web design are application areas, not fundamentals. (You didn't list computer graphics, computer vision, robotics, embedded systems -- all applications, not fundamentals.) You can cover all the set theory and graph theory you need in a day. Most people get this in high school. The stuff you need is just not that complicated. You can safely skip category theory. What you do need is some amount of time spent on the idea that computer programs are mathematical objects which can be reasoned about mathematically. This is the part that the vast majority of people are missing nowadays, and it can be a little tricky to wrap your brain around at first. You need to understand what a fixed point is and why it matters. You need automata theory, but again, the basics are really not that complicated. You need to know about Turing-completeness, and that in addition to Turing machines there are PDAs and FSAs. You need to know that TMs can do things that PDAs can't (like parse context-sensitive grammars), and that PDAs can to things that FSAs can't (like parse context-free grammars) and that FSAs can parse regular expressions, and that's all they can do.
> You need some programming language theory. You need to know what a binding is, and that there are two types of bindings that matter: lexical and dynamic. You need to know what an environment is (a mapping between names and bindings) and how environments are chained. You need to know how evaluation and compilation are related, and the role that environments play in both processes. You need to know the difference between static and dynamic typing. You need to know how to compile a high-level language down to an RTL. For operating systems, you need to know what a process is, what a thread is, some of the ways in which parallel processes lead to problems, and some of the mechanisms for dealing with those problems, including the fact that some of those mechanisms require hardware support (e.g. atomic test-and-set instructions). You need a few basic data structures. Mainly what you need is to understand that what data structures are really all about is making associative maps that are more efficient for certain operations under certain circumstances.
> You need a little bit of database knowledge. Again, what you really need to know is that what databases are really all about is dealing with the architectural differences between RAM and non-volatile storage, and that a lot of these are going away now that these architectural differences are starting to disappear. That's really about it.
>
------------------------------------------------------------------------------------------------------------------------------
## RESOURCES

Philosophy of CS 
Algorithms by Sadwick 
https://computationbook.com/ 
https://www.destroyallsoftware.com/screencasts
https://www.mvanga.com/blog/basic-music-theory-in-200-lines-of-python?utm_source=hackernewsletter&utm_medium=email&utm_term=fav
https://projectlovelace.net/problems/ 
Programming Paradigms 

