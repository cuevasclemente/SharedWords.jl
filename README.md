# SharedWords.jl
This is an implementation of a metric for measuring the ratio of words shared by two shorter strings. This is probably not very useful for large documents, but for simple sentiment analysis, it may be useful.
## Usage
`sharedwords(string1,string2)`

This is one of the main functions used in the metric. Given two strings, it will return the number of words the shorter string shares with the larger, or the number of words shared if both strings are the same size. 

`jarowinkler(string1,string2)`

Calling sharedwords, `jarowinkler` is an implementation of a tokenized Jaro-Winkler metric for two different strings. This implementation returns the difference between 1 and the number of words shared, divided by the length of the smaller string. If the two strings share no words, then similar words will return 0. If the smaller string contains only words that are also contained in the larger string, then similar words will return 1. See the tests for more clarification regarding this.
