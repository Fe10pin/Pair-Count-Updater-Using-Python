# Pair-Count-Updater-Using-Python
This project implements a Python function that updates the frequency count of all ordered pairs of items within a given itemset. The solution uses `defaultdict` from Python’s `collections` module to efficiently track pair occurrences.

from collections import defaultdict

def update_pair_counts(pair_counts, itemset):
    """
    Updates a dictionary of pair counts for
    all pairs of items in a given itemset.
    """
    assert type(pair_counts) is defaultdict

    for a in itemset:
        for b in itemset:
            if a != b:
                pair_counts[(a, b)] += 1


# Demo example
demo_pair_counts = defaultdict(int)
demo_itemset = {'l', 'i', 'o', 'n'}

update_pair_counts(demo_pair_counts, demo_itemset)

print(dict(demo_pair_counts))
