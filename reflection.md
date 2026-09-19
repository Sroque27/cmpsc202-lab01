## 1. At what array size did your baseline algorithm become noticeably sluggish to execute?

Based on my timing results, the baseline algorithm started feeling noticeably slow around n = 2500. Up to about 1000 elements it was still pretty quick, but once it hit 2500 the runtime jumped to around 0.24 seconds, and by 5000 and 10,000 elements it became very slow (almost a full second at 5000 and over 3.7 seconds at 10,000). That’s the point where the quadratic growth really became obvious.

## 2. Based on your empirical data and the shape of your graph, estimate how long (in seconds, minutes, or hours) your baseline algorithm would take to process an array of 1,000,000 elements. Show your reasoning.

My baseline algorithm took about 3.74 seconds at n = 10,000. Since the baseline algorithm is 𝑂(𝑛2), increasing the input size by a factor of 100 (from 10,000 to 1,000,000) increases the runtime by a factor of 1002=10,000.

So the estimate is:

3.74 seconds×10,000=37,400 seconds

37,400 seconds is roughly:

~624 minutes

~10.4 hours

So the baseline algorithm would take around ten hours to process an array of one million elements. This lines up with the steep curve in my plot.

## 3. Based on your empirical data and the shape of your graph, estimate how long (in seconds, minutes, or hours) your Kadane's algorithm would take to process an array of 1,000,000 elements. Show your reasoning.

Kadane’s algorithm took about 0.000848 seconds at n = 10,000. Since Kadane’s algorithm is𝑂(𝑛), increasing the input size by a factor of 100 increases the runtime by the same factor.

So the estimate is:

0.000848×100=0.0848 seconds

That’s under one tenth of a second — basically instant from a user perspective. The plot backs this up because Kadane’s line stays almost flat even as the array size increases.
