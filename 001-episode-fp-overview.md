[Source](https://soundcloud.com/lambda-cast/1-overview-of-functional-programming)

* Functions as first class values means you can pass functions around as if they were strings, integers or any other value. You can declare them, pass them into function, return them from functions.

* Functional programming emphasizes pure functions.

* Imperative languages are time based. Step 1, Step 2, Step 3. The order of execution is important. Imperative is how to do.

* Declarative says what to do. SQL is a good example of an imperative language. 

* Pure a function that takes at least 1 thing. And it has to return something. If it takes arguments it doesn't change them. Any given set of inputs always produce the same output. You can't be rely on system clock, random generators etc. You pass the arguments as values and not by reference. You are passing the copies of them. 

  * length :: String -> Int
* A functions is a mapping from one set of values to another set of values. 

* Total function: for every valid input you will get an output. It called a total function. All pure functions are total.

* Total vs. partial function: If a function always guarantee to give you an answer back then it's total, if not then it's partial. Anything that throws an exception is partial or something that returns null, when it has a declared type e.g. it has to return a String but sometimes returns  a null. Otherwise there could be mapping from one domain to a co-domain. 

* Another example where a function becomes impure when for odd values you return true and non-odd falues you throw or return anything. That is not pure function anymore. It's not deterministic. 

* We are gonna write as much as our program using pure function. One of the big ideas of functional programming. 

* When we want to write in the pure functional style in JavaScript or other non-functional languages we're going to get headaches. But what are else the benefits in doing so in JavaScript. Unit tests, you don't need to mock out things. Mock and stubs don't exist. Mocking is code smell. 

* Pure function don't call impure functions. You're not pure if you're calling an impure function. 

* In fp you have a lot of small functions that are used to in other OOP languages. 

  * map :: Functor f => (a -> b) -> f a -> f b
  * filter : Filterable f => (a -> Bool) -> f a -> f a
  * reduce : Foldable f => (b -> a -> b) -> b -> f a -> b
  
* map, filter, reduce share something in common. They take a function. map, filter, reduce is a higher order function, because it takes another function. 
  
* Lambda: a function that you define as a program is running. You can write the function inline. FP languages generally use a lot of lambdas. 

* There is a lot of benefits you can get through dynamic typing. But many benefits you can only get in static typed languages. 

> Type system in Elm, Haskell is not getting in your way. It's not like in Java. Wher you need all these crazy patterns. Everything of all patterns in Gang of Four book  becomes obsolete. All patterns become just functions. (As Eric Elliot said, the only good thing from the GoF book is the part about object composition.)

* In JavaScript you can solve everything with functions. You don't need all the patterns that are important in the imperative languages. (to me forget: forget the patterns)

* A side effect when a function changes something outside of itself (it's scope). Like making http calls, priting to the console, writing to the database. You can't tell if a function was run. Any mutation of a state (global variable) is a side-effect. 

* All programs start with side-effects (e.g. user input). Functional programs have side-effect, they just have uncontrolled side-effects. The downside of side-effects are hard to reason about it. Pure functions are easy to reason about. By definition they don't have side-effects. 

* What we say control. The language can give you the direction what is pure and what is a side-effect. The side-effects are not bad, it just says you need to keep attention what's going on there. In Haskell IO happens in a type. A function that goes from a string to IO Int (IO means there is side-effect involved). In PureScript it's more specific it goes from Int to Console.log or Ajax Int. While in PureScript this is more general. In PureScript the system is describing what exactly happening. Also there is no way to mix pure with functions with side-effect (control side-effects). In other languages you need to have discipline if you want to mix pure with side-effects. 

* Use pure functions. Use objects as data types like records in Elm/Haskell/Sanctuary. Object only with getters. Not methods, no `this`, no classes etc. 





