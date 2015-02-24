class: center, middle

# CS 312 Help Session - Project 5
### Gene Sequence Alignment

##### Link to my Notes: http://bit.do/project5notes

##### Link to view as slideshow: http://bit.do/project5NotesSlideshow

---

### Objectives

* Design / implement a DP algorithm for the gene sequence alignment problem

* Think carefully about the use of memory in your implementation

* Solve a non-trivial computational genomics problem

* Mature as problem-solvers

---

### Gist of the Project

The project page does an excellent example of detailing what is expected and gives tips on how to implement it:
* [CS 312 Winter 2015: Project 5](http://wiki.cs.byu.edu/cs-312/project-5)

You are using dynamic programming to align multiple gene sequences, two at a time. It is your job in this project to align all pairs in order to assess the pair-wise similarity.

Make sure you understand the sequence alignment and solution extraction algorithms as presented in class. The edit distance algorithm in **section 6.3 of the Dasgupta et al. textbook** is essentially the same algorithm.

---

### Major steps of the problem

* Plan out your data structures, and write pseudo-code. **Note** the two different (though similar) algorithms needed:

  * Scoring algorithm: Simply score the alignment between two sequences but cannot be used to extract the actual alignment.

  * Extraction algorithm: The second algorithm should align the sequences and compute the alignment score (like the first algorithm) but do so in such a way that the actual character-by-character alignment can also be extracted. Call this the “extraction algorithm”.

  * Each algorithm should use DP, in particular the Needleman/Wunsch algorithm. Find the best alignment by minimizing the total cost.

---

### Scoring Algorithm

* Run in at most $O(n^2)$ time and $O(n)$ space; this will require a modification to the algorithm as given in order to be more sparing in the use of space. 
 
* Only align the first 5000 characters (bases) of each sequence.

---

### Continuing with Major Steps

* Your scoring and extraction algorithms should use the following operator costs to compute the distance between two sequences:
 * Substitutions are penalized 1 unit
 * Insertions/Deletions (“indels”) are penalized 5 units
 * Matches are rewarded -3 units

* Implement your algorithm in the PairWiseAlign.Align() method. That method should return the alignment score.

* Record the pair-wise scores computed by the scoring algorithm in the given 10×10 score matrix such that position $(i, j)$ in the display shows the optimal distance from sequencei to sequencej for the first 5000 characters. 

* Only need to fill the upper part of the matrix (above the diagonal). 

---

### Continued

* Use the first two sequences in the database, “polynomial” and “exponential”, to help with debugging

* The optimal alignment of these two strings should be -1 (your code should compute that result for the cell at row 1 and column 2 in the table).
You could also try the operator costs in the book chapter and verify your DP table against the one in the book (see pp. 163-164 in the print textbook).

* Another given example for debugging: (Counting from 1) Row 3, Column 4, should be -14972. That is the result of aligning the first 5000 bases each of the genomes for “Bovine coronavirus isolate BCoV-LUN” and “Bovine coronavirus isolate BCoV-ENT”.

---

### Extraction Algorithm

* This function should produce a character-by-character alignment of its two sequence arguments. 

* This function should not be called to fill the score matrix.

* Add a text field to your GUI for displaying an extracted alignment. 

* Add a click event to the GUI table cells. Further details can be found on the project page.

---

### Continued

* Extract and display the alignment of the first 100 characters of each of the selected sequences in the pair.

* The alignment itself will most likely include gaps and will therefore be longer than 100 characters.

* In case there is more than one optimal alignment, choose one of them.

* For the extra mile, display all of the optimal alignments.

---

### Demonstration

* Now we show a shiny version of the project to see the algorithm in action.

### More Info

Always check the syllabus, project specs for help, try searching Google, then the Google Group for the class, and finally we are available through the TA Email, our office hours, and by appointment. Preferably in that order.

### Questions?
