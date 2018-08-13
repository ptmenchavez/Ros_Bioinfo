
# <font color = 'gold'> Rosalind Bioinformatics Textbook Track </font>
## <font color = 'palevioletred'> Problem BA1C </font>
### Reverse Complement Problem  
<p>
<font color = 'steelblue'>
Find the reverse complement of a DNA string.
    
> Given: A DNA string Pattern.

> Return: Pattern, the reverse complement of Pattern.

```python
# Open data set for problem as file object
test_file = open('rosalind_ba1c.txt', 'r')

# Read file object to save as a variable
test = test_file.read()
test_seq = test.strip()
```

<font color = 'steelblue'>
For this example, a short DNA sequence will be used instead of the actual problem set.
</font>


```python
test_seq = 'ACTGCAT'
```


```python
# Create a dictionary for looking up bases
# Dictionary includes IUPAC codes
# As well as gaps for maintaining input sequence length
complement_bases = {'A' : 'T',
                   'T' : 'A',
                   'C' : 'G',
                   'G' : 'C',
                   'N' : 'N',
                   'R' : 'Y',
                   'Y' : 'R',
                   'S' : 'W',
                   'W' : 'S',
                   'K' : 'M',
                   'M' : 'K',
                   'B' : 'V',
                   'V' : 'B',
                   'D' : 'H',
                   'H' : 'D',
                   '.' : '.',
                   '-' : '-'
                   }

def reverse_complement (seq):
    rev_seq = seq[::-1] # Reverse the seq
    up_rev_seq =  rev_seq.upper() # Make sure all letters are upper case
    base_list = list(up_rev_seq) # Change to list to interate through each base
    rev_comp = [] # Empty list for saving reverse complement look ups
    for base in base_list: # Loop through each base and find it's complement
        add_base = complement_bases.get(base)
        rev_comp.append(add_base)
    rev_comp_str = ''.join(rev_comp) # Change back into a string for proper output
    return rev_comp_str

reverse_complement(test_seq)
```




    'ATGCAGT'



<font color = 'seagreen'>
<b>
Problem solved!
</b>
</font>
