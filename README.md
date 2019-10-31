## Big-O-Notation

Say you order Harry Potter: Complete 8-Film Collection [Blu-ray] from Amazon and download the same film collection online at the same time. You want to test which method is faster. The delivery takes almost a day to arrive and the download completed about 30 minutes earlier. Great! So it’s a tight race.

What if I order several Blu-ray movies like The Lord of the Rings, Twilight, The Dark Knight Trilogy, etc. and download all the movies online at the same time? This time, the delivery still take a day to complete, but the online download takes 3 days to finish.

For online shopping, the number of purchased item (input) doesn’t affect the delivery time. The output is constant. We call this O(1).

For online downloading, the download time is directly proportional to the movie file sizes (input). We call this O(n).

From the experiments, we know that online shopping scales better than online downloading. It is very important to understand big O notation because it helps you to analyze the scalability and efficiency of algorithms.

Note: Big O notation represents the worst-case scenario of an algorithm. Let’s assume that O(1) and O(n) are the worst-case scenarios of the example above.

![big-o-notation complexity](https://i.imgur.com/91u8QEn.png)

**Horrible case 1:**

Any algorithm that calculates all permutation of a given array is O(N!).

```java
void nFacRuntimeFunc(int n) {
  for(int i=0; i<n; i++) {
    nFacRuntimeFunc(n-1);
  }
}
```

**Horrible case 2:**

This program prints out all the moves necessary to solve the famous "Towers of Hanoi" problem for N disks.

[explaination](https://stackoverflow.com/questions/34915869/example-of-big-o-of-2n)

```java
void solve_hanoi(int N, string from_peg, string to_peg, string spare_peg)
{
    if (N<1) {
        return;
    }
    if (N>1) {
        solve_hanoi(N-1, from_peg, spare_peg, to_peg);
    }
    print "move from " + from_peg + " to " + to_peg;
    if (N>1) {
        solve_hanoi(N-1, spare_peg, to_peg, from_peg);
    }
}
```

cc : [http://carlcheo.com/compsci]
