# Individual Homework Assignment 4

## Individual Homework Assignment

This should be completed by each student individually. **You may not work on
this assignment in groups.** Individual assignments are due one week after
being assigned. Remember that your assignment should be well documented
(with a README) and all commit messages should be descriptive.

Your individual assignment is to investigate some nuances related to
floating-point precision. These details often crop up in scientific code,
and can cause issues with repeatability and reproducibility. These issues
are not exclusive to C++, but apply to most languages.

As you have seen, output streams (like `std::cout`) can chop off significant digits
from floating point numbers. We can test this by writing numbers to a file
and then reading them in again, then comparing the numbers.

1. Generate a `std::vector<double>` containing some number of random numbers in the
   range (-10.0 , 10.0). 20 numbers should be good.

1. Write a function that writes a `std::vector<double>` to a file. **Hint** you likely want
   to write the `size()` of the vector to the file first, so the reader known how many
   numbers to read.

1. Write a function that reads that file and returns the `std::vector<double>` of
   file contents. Use this function to re-read the data written in the previous step,
   storing into a different `std::vector<double>`.

1. Check that the sizes of the vector are the same. What might be a good way to make sure
   this is true?

1. Loop over the numbers of both vectors and compare all the elements. Are they equal?

1. You can change the output precision by calling `.precision(n)` on the output filestream.
   What is `n` that causes both the `std::vectors` to be exactly the same? 
