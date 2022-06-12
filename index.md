# well-ordering and deep semantic hashing
```
For example, consider the following two short texts: “I bought an Apple mouse” and “I bought an apple and a mouse”. These two strings are extremely similar in structure.
```

to emphasize this point, let's look at hamming distances:

```
I bought an Apple mouse

$ echo -n 'I bought an Apple mouse' | openssl dgst -sha256 | pbcopy 
30d7bbc8d2dbe6f306cb833b9635a7f535a01069b58163aba5cb1c3dd4221c3a # ...

$ echo -n 'He bought an Apple mouse' | openssl dgst -sha256 | pbcopy 
e3c176b3939dd1266037293b1093d8320a9daa15c54fd72ce56b6ae3e9b8c02c # 59

$ echo -n 'She bought an Apple mouse' | openssl dgst -sha256 | pbcopy 
5d3d6bbdace7336e156f1279b2c20f4908693fc64c41f1a0558836f2195f7afe # 60

 echo -n 'We bought an Apple mouse' | openssl dgst -sha256 | pbcopy 
c9af66c6a1aea977869e84002330e907418aa6b2cf9ce81e2d349ff47eb691e6 # 60

I bought an apple and a mouse

$ echo -n 'I bought an apple and a mouse' | openssl dgst -sha256 | pbcopy
6be41bbfc8203594229a62dc40023e1dc078cb50893ebbde7427645e50b334a8 # 63
```

"there are three things"

```
The set of even numbers and the set {1,5,17,12} with our usual order on numbers are two more examples of well-ordered sets and you can check this

5 + 7 = 12

{5, 7, +, =, 12, 1, 2, 17, 15, 21, 22, 25, 27, 57, 55, 52, 51, 77, 75, 72, 71, 11, 12, 17, 15, ..., 5555, ..., 777777111111111, ..., 1===1, ..., ++5, ..., ++++++++++++++++++++++++++.....++++++++, ...}

{-[...], -[...], +[...], +[...]}
```

maintaining symmetric relation despite the possibility of gödel numbering

we might ask, e.g., if the qualitative properties of the hashing distance, or semantic distance, taken over a temporal period between two hashes in a public proof-of-work blockchain will tell us anything about the likelihood of the outcome of the hash cracking scheme.

```
# proof-of-work hash crashing
...

# 3 min ago (lower similarity in structure)
0000000000000000000665a9ce7726c84b960de09f84e4be37163163efc7ea50 # ...

# 50 min ago (temporal progression)
000000000000000000036bbcab6a71f5bb1f3751b91e56f7297ca578458ca375 # 43

# 6 hours ago (higher similarity in structure)
000000000000000000021b24b4f3268972fc4053bfc5ad90aef73f3d9a873cec # 40
```

by [the law of large numbers](https://en.wikipedia.org/wiki/Law_of_large_numbers) we should expect that with smaller positive integers we are tracking, we should more likely predict their hash if we know some N quantity of transactions (i.e., assuming we know /any/ order at all). however, by measuring hamming distances (similarity) we know that the more data we have there is a higher ordered value equal to or greater than N. the less we know, the better we can predict. 

fun

[0]: "Deep Semantic Hashing. Matthew Findlay Isaac Jorgensen Esai Morales Kevin Velcich. June 12, 2018.
[1]: "The Well-Ordering Theorem: one of the Greatest Mathematical Controversies of All Time": "Recall that the set of natural numbers with the order < is well-ordered. In general, a set (such as N) with some order (<) is called well-ordered if any nonempty subset has a least element. The set of even numbers and the set {1,5,17,12} with our usual order on numbers are two more examples of well-ordered sets and you can check this. However, the set of integers with our usual ordering on it is not well-ordered, neither is the set of rational numbers, nor the set of all positive rational numbers."
