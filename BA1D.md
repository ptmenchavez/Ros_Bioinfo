
# <font color = 'gold'> Rosalind Bioinformatics Textbook Track </font>
## <font color = 'palevioletred'> Problem BA1D </font>
### Pattern Matching Problem
<p>
    <font color = 'steelblue'>
        Final all occurrences of a pattern in a string
        
> Given: Strings Pattern and Genome.
        
> Return: All starting positions in Genome where Pattern appears as a substring. Use 0-based indexing.
        
</font>


```python
def patt_match(pattern, genome):
    matched_ind = list() #Emply list for saving start positions
    patt_len = len(pattern)
    genome_end = len(genome) - patt_len + 1
    for i in range(0, genome_end):
        test_match = genome[i : i + patt_len]
        if pattern == test_match:
            matched_ind.append(i)
    return matched_ind
```

<font color = 'steelblue'>
    Let's test the function.
    </font


```python
print(patt_match('CAT', 'ACATATCAGCATGCATCATGTCAT'))
```

    [1, 9, 13, 16, 21]


<font color = 'steelblue'> For submission, remember to remove all the commas. </font>

<font color = 'seagreen'> <b> Problem solved! </font></b>
