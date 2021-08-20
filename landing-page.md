# Testing how you test (with replit)

How would you check that a function like `fib` does what you expect it to? Try running `fib(x)` in the console below for different numbers `x`. Does it give you what you expect?

<iframe frameborder="0" width="100%" height="500px" src="https://replit.com/@patrickmineault/Writing-tests?lite=true"></iframe>

```{hint}
Try running `fib(0)`, `fib(1)`, `fib(10)`. Check against the [encyclopedia of integer sequences](https://oeis.org/search?q=fibonacci&language=english&go=Search). Do the results agree? What about `fib(-1)`? How would you treat unusual cases like this?
```

Through our detective work, we notice that we have an off-by-one error! Indeed, the true sequence goes:

$F(x) = {0, 1, 1, 2, \ldots}$

While we programmed:

$F'(x) = {1, 1, 2, 3 \ldots}$

These kinds of subtle mistakes happen all the time when we write scientific code. That's why:

> Most scientists who write software constantly test their code. That is, if you are a scientist writing software, I am sure that you have tried to see how well your code works by running every new function you write, examining the inputs and the outputs of the function, to see if the code runs properly (without error), and to see whether the results make sense. Automated code testing takes this informal practice, makes it formal, and automates it, so that you can make sure that your code does what it is supposed to do, even as you go about making changes around it. --Ariel Rokem, Shablona README

So let's fix our code, and create tests to check that our code works as expected. That way, if we make another mistake in our code, the tests will catch it!