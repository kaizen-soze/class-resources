# Break problems down with pseudocode

When you're working on an issue, it can be tempting to just jump in and start coding. This is usually not a great idea.

Problems are typically more complex than they initially appear, and if you just start coding without considering how to solve the overall problem you may code yourself into a corner.

One useful tool for breaking down complex problems is with an approach called `pseudocode`.

Pseudocode involves writing down, step by step, how to solve a problem. Once you have the approach figured out it's much easier to start coding.

Let's say you're writing code that is intended to process payment from a customer.

There are a lot of moving parts for a something like this, and you have to be sure that you haven't missed anything. Pseudocode is an ideal tool to get started down the right path.

```
// Validate user information:
// Name
// Email
// Address
// Credit Card Number

// Validate all product information:
// Product Name
// Product price
// Tax
// Total price to be charged

// Send information securely to our payment processor

// Process the response from our payment processor

// Update our local database

// Display result of transaction to user

```

Pseudocode can be as high-level or as low-level as required in order to solve the problem at hand. The example above is high-level; it's light on details. However, it gives you a starting point to start doing the appropriate research to solve the other problems.

Low-level pseudocode is more appropriate for things like individual methods.

If you were writing pseudocode for a method that finds how many words in a sentence have the letter `a` in them, your pseudocode could look like this:

```
// Split the sentence into an array of words

// Loop through the array

    // Test each letter to see if the target letter is a match

    // If found, increase our counter variable by one

// Return the value of our counter
```

Once you have your approach mapped out and you're reasonably sure it works, you are ready to start coding.

Some general rules of thumb:

* Pseudocode should be language-independent
* Pseudocode should be written in plain english. This allows it to be shared with a non-technical audience
* Pseudocode doesn't need to be used for every problem, but it can be helpful to break the overall problem down if there is uncertainty or if you don't yet know the solution to the problem you're trying to solve.


