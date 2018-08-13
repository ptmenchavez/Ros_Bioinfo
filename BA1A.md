
# <font color = 'gold'> Rosalind Bioinformatics Textbook Track </font>
## <font color = 'palevioletred'> Problem BA1A </font>
### Compute the Number of Times a Pattern Appears in a Text
<p>
<font color = 'steelblue'>
Implement PatternCount
    
> Given: {DNA strings}} Text and Pattern

> Return: Count(Text, Pattern)

</font>


```python
# PatternCount function will take a text and pattern
# The function will then look for how many times the pattern occurs within the text

def PatternCount(text, pattern):
    p_len = len(pattern)
    end_pos = len(text)-p_len
    count = 0
    matches = []
    for i in range(0, end_pos+1):
        test = text[i:i + p_len]
        if test == pattern:
            count = count + 1
            matches.append(i)
    print(count)
```

<font color = 'steelblue'>
    Let's test the function.
</font>


```python
PatternCount('ATCATCTACATGAT', 'CAT')
```

    2


<font color = 'seagreen'>
<b>
Problem solved!
</b>
</font>
