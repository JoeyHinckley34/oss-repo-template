# Lab 6 Scientific Computation
### Five letter words
<img width="1075" alt="Screen Shot 2022-03-14 at 6 28 20 PM" src="https://user-images.githubusercontent.com/50917542/158271359-71018a19-9609-4d47-9745-00f38889bec7.png">
I changed the output so it looked cleaner and fits in one page


### Four letter words
<img width="501" alt="Screen Shot 2022-03-14 at 6 46 11 PM" src="https://user-images.githubusercontent.com/50917542/158273098-420ec91a-6df3-4683-b622-2efa94c0460c.png">

### 5 letter words ingoring order
<img width="456" alt="Screen Shot 2022-03-14 at 7 09 41 PM" src="https://user-images.githubusercontent.com/50917542/158275393-425cf53f-d15b-426c-aacf-ef6f26a61c88.png">
```
"""
=====
Words
=====

Words/Ladder Graph
------------------
Generate  an undirected graph over the 5757 5-letter words in the
datafile `words_dat.txt.gz`.  Two words are connected by an edge
if they differ in one letter, resulting in 14,135 edges. This example
is described in Section 1.1 in Knuth's book (see [1]_ and [2]_).

References
----------
.. [1] Donald E. Knuth,
   "The Stanford GraphBase: A Platform for Combinatorial Computing",
   ACM Press, New York, 1993.
.. [2] http://www-cs-faculty.stanford.edu/~knuth/sgb.html
"""
# Authors: Aric Hagberg (hagberg@lanl.gov),
#          Brendt Wohlberg,
#          hughdbrown@yahoo.com

#    Copyright (C) 2004-2019 by
#    Aric Hagberg <hagberg@lanl.gov>
#    Dan Schult <dschult@colgate.edu>
#    Pieter Swart <swart@lanl.gov>
#    All rights reserved.
#    BSD license.

import gzip
from string import ascii_lowercase as lowercase
from itertools import permutations
import networkx as nx

#-------------------------------------------------------------------
#   The Words/Ladder graph of Section 1.1
#-------------------------------------------------------------------


def generate_graph(words):
    G = nx.Graph(name="words")
    lookup = dict((c, lowercase.index(c)) for c in lowercase)

    def edit_distance_one(word):
        #gets all the possible permuations of the word as a list
        perm = list(permutations(word))
        for i in perm:
            #for each permuation join the list together into one string
            w = "".join(i)
            for z in range(len(word)):
                left, c, right = w[0:z], w[z], w[z + 1:]
                j = lookup[c]  # lowercase.index(c)
                for cc in lowercase[j + 1:]:
                    yield left + cc + right
    candgen = ((word, cand) for word in sorted(words)
               for cand in edit_distance_one(word) if cand in words)
    G.add_nodes_from(words)
    for word, cand in candgen:
        G.add_edge(word, cand)
    return G


def words_graph():
    """Return the words example graph from the Stanford GraphBase"""
    fh = gzip.open('words_dat.txt.gz', 'r')
    words = set()
    for line in fh.readlines():
        line = line.decode()
        if line.startswith('*'):
            continue
        w = str(line[0:5])
        words.add(w)
    return generate_graph(words)


if __name__ == '__main__':
    G = words_graph()
    print("Loaded words_dat.txt containing 5757 five-letter English words.")
    print("Two words are connected if they differ in one letter.")
    print("Graph has %d nodes with %d edges"
          % (nx.number_of_nodes(G), nx.number_of_edges(G)))
    print("%d connected components" % nx.number_connected_components(G))

    for (source, target) in [('chaos', 'order'),
                            ('plots', 'graph'),
                            ('moron', 'smart'),
                            ('flies', 'swims'),
                            ('mango', 'peach'),
                            ('pound', 'marks')]:
        print("Shortest path between %s and %s is" % (source, target))
        try:
            sp = nx.shortest_path(G, source, target)
            for n in range(len(sp)):
                if (n != len(sp)-1):
                    print(sp[n],end=' -> ')
                else:
                    print(sp[n])
        except nx.NetworkXNoPath:
            print("None")

```
