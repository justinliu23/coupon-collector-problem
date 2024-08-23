# coupon-collector-problem
 
This document explores the statistical problem known as the Coupon Collector's Problem. It includes both theoretical explanations and practical implementations.

For a situation of `n` distinct tickets, the function `coupon_collector` initiates a list `collected` which is populated with `n` false values. It has two counter variables: `count`, which keeps track of how many trials have been run thus far, and `distinct`, which keeps track of how many of the distinct tickets have been collected thus far. Each time a coupon is collected, it is independently chosen at random from a set of `n` different types. This randomness in selection means that you cannot predict which coupon you will get in any given trial.

While the value of `distinct` is less than the `n` total tickets, the code has a chance of collecting a distinct ticket. If this distinct ticket has not been logged, then we collect a new ticket and update our counters accordingly.

## Mathematical Background

The probability of collecting all `n` distinct tickets can be described using the following equation:

```math
P(n) = n \cdot (1 - \frac{1}{n})^{n-1}
```

This equation provides the probability of having collected all distinct tickets after `n` trials.

## Implementation

The implementation details are as follows:

1. Initialize a boolean list of size `n` to track collected tickets.
2. Randomly select a ticket in each trial and update the list.
3. Continue until all tickets are collected.
