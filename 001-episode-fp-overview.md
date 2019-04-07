[Source](https://soundcloud.com/lambda-cast/1-overview-of-functional-programming)

* Functions as first class values means you can pass functions around as if they were strings, integers or any other value. You can declare them, pass them into function, return them from functions.

* Functional programming emphasizes pure functions.

* Imperative languages are time based. Step 1, Step 2, Step 3. The order of execution is important. Imperative is how to do.

* Declarative says what to do. SQL is a good example of an imperative language. 

* Pure a function that takes at least 1 thing. And it has to return something. If it takes arguments it doesn't change them. Any given set of inputs always produce the same output. You can't be rely on system clock, random generators etc. You pass the arguments as values and not by reference. You are passing the copies of them. 

length :: String -> Int
* A functions is a mapping from one set of values to another set of values. 

* Total function: for every valid input you will get an output. It called a total function. All pure functions are total.

* Total vs. partial function: If a function always guarantee to give you an answer back then it's total, if not then it's partial. Anything that throws an exception is partial or something that returns null, when it has a declared type e.g. it has to return a String but sometimes returns  a null. Otherwise there could be mapping from one domain to a co-domain. 

* Another example where a function becomes impure when for odd values you return true and non-odd falues you throw or return anything. That is not pure function anymore. It's not deterministic. 

* We are gonna write as much as our program using pure function. One of the big ideas of functional programming. 

* When we want to write in the pure functional style in JavaScript or other non-functional languages we're going to get headaches. But what are else the benefits in doing so in JavaScript. Unit tests, you don't need to mock out things. Mock and stubs don't exist. Mocking is code smell. 

* Pure function don't call impure functions. You're not pure if you're calling an impure function. 

* In fp you have a lot of small functions that are used to in other OOP languages. 

map :: Functor f => (a -> b) -> f a -> f b

