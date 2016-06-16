randomProjections
=================
An algorithm to discover motifs(recurring contiguous subsequences) in symbolic data.

Terminology
-----------

 * data: Long string containing instances of planted or real motifs, flawed by up to a specified number of differences from the model.
 * n: Length of data
 * Motif: recurring contiguous subsequence in data, containing some noise.
 * L: Length of motif searched for.
 *
 * |c|, #c: cardinality of datastructure/collection c.

 * Noise, differences, distortions, deviations: mismatches of model and instance of motif.
 * support of a motif/model: Amount of occurrences of motif/model in data.

 * ĸ-scatter of s: String that is concatenation of characters s[i] where i in ĸ. ĸ is a collection of integers.
     'Mathematical' notation: [ s[i] | i in ĸ]. Length of ĸ-scatter: |k|.
 * k: Array or collection containing up to L-d random indices where L is the length of the motif and d is the error tolerance.
     If there were more indices, the k-scatter and the set of indices of deviations in a motif could never be disjoint.
 The indices can be in the range [0, L-1].

 * Friend: 2 strings a and  b in data are defined to be friends if they share some k-scatters
     (i.e. if for some random projections, the scatters of a and b are equal).