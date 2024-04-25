# Molecular-Clock
<b><i>Definitions of functions used:</i></b>

1. <b><i>FrequentWords</i></b>: Program to find kmer of length <b>k</b> with maximum frequency in <b>Text</b>

2. <b><i>HammingDistance</i></b>: Program to find the number of mismatches (position wise) between two same length strings

3. <b><i>Neighbors</i></b>: Program to generate the set of all k-mers whose <b>Hamming distance</b> from <b>Pattern</b> does not exceed <b>d</b>

4. <b><i>MotifEnumeration</i></b>: Program to find motifs of length <b>k</b> with atmost <b>d</b> mismatches in all strings in <b>Dna</b> by generating a neighbourhood of motifs using <b>Neighbors</b> function

5. <b><i>entropy</i></b>: Program to score motif matrix. It scores individual instances of motifs depending on how similar they are to a consensus. 

6. <b><i>DistanceBetweenPatternAndStrings</i></b>: 