# Molecular-Clock
<b><i>Definitions of functions used:</i></b>

1. <b><i>FrequentWords</i></b>: Program to find kmer of length <b>k</b> with maximum frequency in <b>Text</b>

2. <b><i>HammingDistance</i></b>: Program to find the number of mismatches (position wise) between two same length strings

3. <b><i>Neighbors</i></b>: Program to generate the set of all k-mers whose <b>Hamming distance</b> from <b>Pattern</b> does not exceed <b>d</b>

4. <b><i>MotifEnumeration</i></b>: Program to find motifs of length <b>k</b> with atmost <b>d</b> mismatches in all strings in <b>Dna</b> by generating a neighbourhood of motifs using <b>Neighbors</b> function

5. <b><i>entropy</i></b>: Program to score motif matrix. It scores individual instances of motifs depending on how similar they are to a consensus. 

6. <b><i>DistanceBetweenPatternAndStrings</i></b>: Program to find sum of all <b>Hamming distance</b> of a pattern from a collection of strings

7. <b><i>median_string</i></b>: Program to find the collection of kmers of length <b>k</b> that minimizes the <b>Hamming distance</b> between the kmer and a collection of strings in which the probable motif is present

8. <b><i>Profile_MostProbable_kmer</i></b>: Program to find the most probable kmer of length <b>k</b> present in the <b>string</b> using the probabilities given in the <b>profile</b>

9. <b><i>greedy_motif_search</i></b>: Uses greedy algorithm for motif finding. It aims to find a collection of motifs of length <b>k</b> from a set of DNA sequences (total <b>t</b> sequences) that are most likely to be conserved across these sequences. It does this by iteratively building motifs based on a probabilistic profile and compare their scores to find the best set of motifs with the lowest score, indicating higher conservation

    <b>form_profile</b>: Generates a profile matrix from a list of motifs
    <b>profile_most_probable_kmer</b>: Finds the most probable k-mer in a sequence based on a given profile matrix
    <b>score_motifs</b>: Calculates the score of a list of motifs, which typically measures how conserved the motifs are

10. <b><i>improved_greedy_motif_search</i></b>: Follows the same algorithm as greedy motif search except it uses <b>Laplace's rule of Succession</b> to use pseudocounts in forming the profile matrix

11. <b><i>Randomized_Motif_Search</i></b>: Program uses a randomized approach combined with an iterative improvement strategy to find motifs

    <b>Random_Motifs</b>: Generates initial random motifs from the DNA sequences
    <b>form_profile_pseudocounts</b>: Creates a profile matrix with pseudocounts from a list of motifs
    <b>Generate_Motifs</b>: Generates new motifs based on the profile matrix and DNA sequences
    <b>Score</b>: Calculates the score of a list of motifs, which typically measures how conserved the motifs are

It uses <b>Run_Randomized_Motif_Search</b> to run the program iteratively and converge to the best solution governed by the least score

12. <b><i>GibbsSampler</i></b>: Program uses a stochastic iterative process known as Gibbs Sampling, a type of Markov Chain Monte Carlo (MCMC) algorithm to find motifs

    <b>ProfileRandomlyGeneratedKmer</b>: Generates a k-mer from a DNA sequence based on the given profile probabilities

It uses <b>runGibbsSampler</b> to run the program iteratively and converge to the best solution governed by the least score as well as uses <b>N</b> for N random starts of the program
