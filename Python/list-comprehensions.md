List Comprehensions
---

Python has a very powerful tool which can create a new list from an existing list, in a single, readable line.

#### Example 1
Let's say we have a list of names, but they may have additional spaces as well. And, we need a new list carrying the names, but not the spaces.

One may write the following code for it:

```
list_containing_names_with_spaces = [" sachin  ", " dravid   ", "laxman   "]
clean_list=[]
for name in list_containing_names_with_spaces:
    clean_list.append(name.strip())
print(clean_list)
```

However, with list comprehension, you can convert the above code into:

```
list_containing_names_with_spaces = [" sachin  ", " dravid   ", "laxman   "]
clean_list=[name.strip() for name in list_containing_names_with_spaces]
print(clean_list)
```

#### Example 2
One can even have a conditional statement while comprehending a list.

Let's say we need to create a list of integers which specify the length of each word in a certain sentence, but only if the word is not the word "the".

```
sentence = "the quick brown fox jumps over the lazy dog"
words = sentence.split()
word_lengths = []
for word in words:
    if word != "the":
        word_lengths.append(len(word))
```

Using list comprehensions, the above code will turn into:

```
sentence = "the quick brown fox jumps over the lazy dog"
words = sentence.split()
word_lengths = [len(word) for word in words if word != "the"]
```
