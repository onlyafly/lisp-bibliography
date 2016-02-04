# A Lisp Bibliography

A bibliography of reading material on Lisps (Common Lisp, Scheme, Clojure, etc.) and related research. Sometimes only quite vaguely related...

I prefer resources that are broadly applicable over ones that are highly specific, which means that I am heavy on things that teach you ideas and concepts over technologies. Technologies are transitory, while concepts will be with you forever.

**Grading Key:**
 * 3 - Must read for all developers.
 * 2 - Every developer interested in the topic should see/read it.
 * 1 - Could be useful for developers interested in the topic.

**Todo:**
* Move relevant content from here: https://docs.google.com/document/d/1A0EVj7f4DUTjbFs4OLqkPJe-WZKG-NvIn5CTgc2F1lI/edit?hl=sv#heading=h.t43faihoaeuo

## Meta Lists

* [Clojure the Next Level](http://www.lispcast.com/clojure-the-next-level)
* [Rich Hickey’s Greatest Hits](https://changelog.com/rich-hickeys-greatest-hits/)
  * The greatest videos from Rich Hickey, creator or Clojure and all-around programmer-philosopher.
* [Free Programming Books](https://github.com/vhf/free-programming-books/blob/master/free-programming-books.md)
  * List of legal and free programming books.
* [Papers We Love](http://paperswelove.org/)
  * Repository of academic computer science papers and a community who loves reading them.
* [JS Must Watch](https://github.com/bolshchikov/js-must-watch/tree/master)
  * Curated list of the best JS videos over the years.

## In Defense of Programming Languages

* ["Why Does The World Need More Programming Languages?" by Chris Dannen](http://www.fastcolabs.com/3031443/why-does-the-world-need-more-programming-languages)
* ["The Hundred-Year Language" by Paul Graham](http://paulgraham.com/hundred.html)
* ["Why we need even more programming languages" By Neil McAllister](http://www.infoworld.com/article/2618643/application-development/why-we-need-even-more-programming-languages.html)
  * Upgrading existing, popular languages to support new features is a lot harder than you might think

## Concurrency

### Multiversion Concurrency Control / Transactional Memory

* ["Are We There Yet?" by Rich Hickey (Presentation)](http://www.infoq.com/presentations/Are-We-There-Yet-Rich-Hickey) -- 3/3
  * Philosophical discussion of identity/state/time, and a practical discussion on MVCC and STM.

### Communicating Sequential Processes

* ["Communicating Sequential Processes (Wikipedia)"](http://en.wikipedia.org/wiki/Communicating_sequential_processes)

Lisps that are influenced by CSP:

- Clojure's core.async:
  - https://github.com/clojure/core.async/
  - Rich Hickey on core.async:
    http://www.infoq.com/presentations/clojure-core-async
  - http://swannodette.github.io/2013/07/12/communicating-sequential-processes/

Go's Concurrency Patterns:

* http://blog.golang.org/share-memory-by-communicating
* http://blog.golang.org/go-concurrency-patterns-timing-out-and
* http://blog.golang.org/pipelines
* http://blog.golang.org/context

## Lisp Implementation

### Implementing Macros

- First-class macros: http://matt.might.net/articles/metacircular-evaluation-and-first-class-run-time-macros/
- https://xivilization.net/~marek/blog/2013/09/17/clojure-and-hygienic-macros/

## Monads

- http://www.infoq.com/presentations/Why-is-a-Monad-Like-a-Writing-Desk¨

## Scheme/Lisp

- http://c2.com/cgi/wiki?ImplementingLisp
- “Structure and Interpretation of Computer Programs”
  - HTML book: http://mitpress.mit.edu/sicp/full-text/book/book.html
  - Video Lectures: http://ocw.mit.edu/courses/electrical-engineering-and-computer-science/6-001-structure-and-interpretation-of-computer-programs-spring-2005/video-lectures/
  - Kindle book: https://github.com/jonathanpatt/sicp-kindle
- "Scheme from Scratch" by Peter Michaux: http://peter.michaux.ca/articles/scheme-from-scratch-introduction

## Compiler/Interpreter Phases

### Parsing

- Parser: https://golang.org/src/go/parser/parser.go
- Error handling: https://golang.org/src/go/scanner/errors.go

### Analysis

- https://golang.org/src/go/ast/walk.go



### Compilation

#### Compiling to C-like

- Chicken Scheme
- Clojure???
- http://matt.might.net/articles/compiling-scheme-to-c/

#### Implementing Tail Recursion

- "A little bit of CPS, a few thunks, and a trampoline" by Chris Frisz (Video): http://www.chrisfrisz.com/slides/clojure-tco.pdf
  - Short presentation on how TCO was implemented on top of Clojure
- "CONS Should Not CONS Its Arguments, Part II: Cheney on the M.T.A." by Henry Baker: http://home.pipeline.com/~hbaker1/CheneyMTA.html
  - Describes a technique to implement full tail recursion when compiling from Scheme into C.
- The Scheme2JS compiler and especially its trampoline implementation has been presented: http://www-sop.inria.fr/indes/scheme2js/files/tfp2007.pdf
- "The 90 Minute Scheme to C compiler" by Marc Feeley: http://www.iro.umontreal.ca/~boucherd/mslug/meetings/20041020/minutes-en.html
  - Supports fully optimized proper tail calls, continuations, and (of course) full closures, using two important compilation techniques for functional languages: closure conversion and CPS-conversion
- http://www.cs.indiana.edu/~dyb/papers/3imp.pdf

#### Implementing call/cc

- Description of Scheme2Js's call/cc implementation: http://www-sop.inria.fr/indes/scheme2js/files/schemews2007.pdf

### Typing

- http://docs.racket-lang.org/ts-guide/
