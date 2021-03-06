# Codility

## Sample Problems

- [Cover Buildings](https://app.codility.com/programmers/task/cover_buildings/)
- [RectangleStrip](https://app.codility.com/programmers/task/rectangles_strip/)

Write tests first, using the sample inputs and result given.

During an Animal Day event, N people (numbered from 0 to N−1) showed up. Each of them had either a dog or a cat. The organizers decided to give them a wonderful gift: a toy for each animal.

After the event, it turned out that some people who owned a dog had received a cat-toy, and some people who owned a cat received a dog-toy. People may exchange toys, but only if they know each other (otherwise they have no way to contact the other person). The pair of people can exchange toys multiple times.

Knowing who knows who, who owns which animal, and what kind of toy he or she received, can you determine whether it is possible for people to exchange toys in such a way that every dog ends up with a dog-toy and every cat gets a cat-toy?

Write a function:

class Solution { public boolean solution(int[] P, int[] T, int[] A, int[] B); }

that returns true if it is possible to exchange toys in such a way that every animal receives an appropriate toy, or false otherwise. First two arrays describe the pets (array P) and toys (array T) that every person owns. The J-th person owns pet P[J] and toy T[J] (1 means dog or dog-toy and 2 means cat or cat-toy). The next two arrays, A and B, both of length M, describe the relationships between people. For each integer K from 0 to M−1, person A[K] knows person B[K].

Examples:

1. Given:

P = [1, 1, 2]
T = [2, 1, 1]
A = [0, 2]
B = [1, 1]
the function should return true. Person 0 can exchange toys with person 1 to obtain a dog-toy, and then person 1 can exchange toys with person 2.

2. Given:

P = [2, 2, 1, 1, 1]
T = [1, 1, 1, 2, 2]
A = [0, 1, 2, 3]
B = [1, 2, 0, 4]
the function should return false. There is no way for persons 3 and 4 to exchange toys with others.

3. Given:

P = [1, 1, 2, 2, 1, 1, 2, 2]
T = [1, 1, 1, 1, 2, 2, 2, 2]
A = [0, 2, 4, 6]
B = [1, 3, 5, 7]
the function should return false. There is no way for persons 2 and 3 and for persons 4 and 5 to exchange toys with others.

4. Given:

P = [2, 2, 2, 2, 1, 1, 1, 1]
T = [1, 1, 1, 1, 2, 2, 2, 2]
A = [0, 1, 2, 3, 4, 5, 6]
B = [1, 2, 3, 4, 5, 6, 7]
the function should return true.

Write an efficient algorithm for the following assumptions:

N is an integer within the range [1..100,000];
M is an integer within the range [0..200,000];
each element of array ('P', 'T') is an integer that can have one of the following values: 1, 2;
each element of arrays A, B is an integer within the range [0..N−1];
for each integer K from 0 to M−1, elements A[K] and B[K] are different;
there are no redundant elements in arrays A, B; more formally every unordered pair of persons a, b will appear as A[K], B[K] for at most one K.
Copyright 2009–2021 by Codility Limited. All Rights Reserved. Unauthorized copying, publication or disclosure prohibited.


Example test:   ([1, 1, 2], [2, 1, 1], [0, 1], [1, 2])
Output:
Index 0 doesn't match
Swapping index 0 and 1
Index 1 doesn't match
Swapping index 1 and 2
Index 2 matches
OK

Example test:   ([2, 2, 1, 1, 1], [1, 1, 1, 2, 2], [0, 1, 2, 3], [1, 2, 0, 4])
Output:
Index 0 doesn't match
Swapping index 0 and 2
Index 1 doesn't match
Swapping index 1 and 2
Index 2 matches
Index 3 doesn't match
Swapping index 3 and 4
Index 4 doesn't match
Swapping index 4 and 3
Final Check 0 doesn't match
OK

Example test:   ([1, 1, 2, 2, 1, 1, 2, 2], [1, 1, 1, 1, 2, 2, 2, 2], [0, 2, 4, 6], [1, 3, 5, 7])
Output:
Index 0 matches
Index 1 matches
Index 2 doesn't match
Swapping index 2 and 3
Index 3 doesn't match
Swapping index 3 and 2
Index 4 doesn't match
Swapping index 4 and 5
Index 5 doesn't match
Swapping index 5 and 4
Index 6 matches
Index 7 matches
Final Check 2 doesn't match
OK

Example test:   ([2, 2, 2, 2, 1, 1, 1, 1], [1, 1, 1, 1, 2, 2, 2, 2], [0, 1, 2, 3, 4, 5, 6], [1, 2, 3, 4, 5, 6, 7])
Output:
Index 0 doesn't match
Swapping index 0 and 1
Index 1 doesn't match
Swapping index 1 and 2
Index 2 doesn't match
Swapping index 2 and 3
Index 3 doesn't match
Swapping index 3 and 4
Index 4 matches
Index 5 doesn't match
Swapping index 5 and 6
Index 6 doesn't match
Swapping index 6 and 7
Index 7 doesn't match
Swapping index 7 and 6
Final Check 0 doesn't match
WRONG ANSWER (got False expected True)

Producing output might cause your solution to fail performance tests.
You should remove code that produces output before you submit your solution.

Detected some errors.