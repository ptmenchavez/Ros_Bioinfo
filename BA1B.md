
# <font color = 'gold'> Rosalind Bioinformatics Textbook Track </font>
## <font color = 'palevioletred'> Problem BA1B </font>
### Frequent Words Problem
<p>
    <font color = 'steelblue'>
                   Find the most frequent k-mers in a string.

> Given: A DNA string Text and an integer k.

> Return: All most frequent k-mers in Text (in any order).
</font>


```python
# Function will take a string, text, and integer, k
# Function will then find the most frequent k-mer and print them out 
def freq_kmer(text, k):
    k_dict = dict()
    i = 0
    end = len(text) - k + 1
    while i < end:
        curr_k = text[i:i+k]
        k_dict[curr_k] = k_dict.get(curr_k, 0) + 1
        i += 1
    max_kmer = max(k_dict, key = k_dict.get) # Find a key (any key) with the maximum value
    max_count = k_dict[max_kmer]
    # print(max_count)
    for k, v in k_dict.items():
        if v == max_count:
            print(k)
```

<font color = 'steelblue'>
    Let's test the function out.


```python
freq_kmer('CATCATTAGGTACGATAGTAGCATAG', 3)
```

    TAG


<font color = 'seagreen'>
    <b>Problem solved!</b>
</font>
