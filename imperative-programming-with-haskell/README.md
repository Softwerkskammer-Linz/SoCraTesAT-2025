# Imperative Programming with Haskell

## Why?

Imperative style is for many tasks useful and less academic than a pure functional one.

For instance, in Haskell it turns something like:

```haskell
main = print "What's your name?" >> getLine >>= \n -> print "Hello, " ++ n ++ "!"
```

into

```haskell
main = do
  print "What's your name?"
  n <- getLine
  print "Hello, " ++ n ++ "!"
```

Purists claim that do-notation should be avoided. See also [Do Notation considered harmful](https://wiki.haskell.org/Do_notation_considered_harmful).

I don't agree. Imperative style is for the most programmers more understandable and combines the benefits of safe and efficient handling for effectful tasks with a familiar programming style. While when going fully FP you will perform a complete paradigm shift.

## Use Cases

* Working with I/O
* Working with Optional values (in Haskell the Maybe data type)
* Working with Error Handling (in Haskell the Either data type)

## Do Notation in other programming languages

* Arrow-Kt offers for Kotlin the same style for many data types: https://arrow-kt.io/learn/typed-errors/working-with-typed-errors/
* Effect Js has with `Effect.gen` a similar feature for JS/TS: https://effect.website/docs/getting-started/using-generators/
* Scala has **for comprehensions** for data types sharing (monadic) features: https://docs.scala-lang.org/tour/for-comprehensions.html
* Fsharp has **computational expressions**: https://learn.microsoft.com/en-us/dotnet/fsharp/language-reference/computation-expressions
* Rust allows to work with the `?` operator for Option and Result that enable imperative programming: https://doc.rust-lang.org/std/option/#the-question-mark-operator-
* Any programming language with `async`/`await` allows imperative programming for Promises.

## Other Resources

* Source Repo I used for my demo on GitHub: https://github.com/enolive/fancy-police/

