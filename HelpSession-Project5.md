class: center, middle

# CS 312 Help Session - Project 5
### Gene Sequence Alignment

##### Link to my Notes: http://bit.do/project5notes

##### Link to view as slideshow: http://bit.do/project5slides

---

# Objectives

* Design / implement a DP algorithm for the gene sequence alignment problem

* Think carefully about the use of memory in your implementation

* Solve a non-trivial computational genomics problem

* Mature as problem-solvers

---

# Gist of the Project

The project page does an excellent example of detailing what is expected and gives tips on how to implement it:
* [CS 312 Winter 2015: Project 5](http://wiki.cs.byu.edu/cs-312/project-5)

You are using dynamic programming to align multiple gene sequences, two at a time. It is your job in this project to align all pairs in order to assess the pair-wise similarity.

Make sure you understand the sequence alignment and solution extraction algorithms as presented in class. The edit distance algorithm in **section 6.3 of the Dasgupta et al. textbook** is essentially the same algorithm.

---

# Major steps of the problem

1. Plan out your data structures, and write pseudo-code for the alignment and extraction algorithms that you need to implement. **Note** the two different (though similar) algorithms needed:
  * Scoring algorithm: Simply score the alignment between two sequences but cannot be used to extract the actual alignment.
  * Extraction algorithm: The second algorithm should align the sequences and compute the alignment score (like the first algorithm) but do so in such a way that the actual character-by-character alignment can also be extracted. Call this the “extraction algorithm”.
  * Each algorithm should use DP, in particular the Needleman/Wunsch algorithm. Find the best alignment by minimizing the total cost.
The requirement is that your scoring algorithm run in at most O(n2) time and O(n) space; this will require a modification to the algorithm as given in order to be more sparing in the use of space. On the other hand, your extraction algorithm can use O(n2) in time and space, as shown in class and practiced in the homework.
Your scoring and extraction algorithms should use the following operator costs to compute the distance between two sequences:
Substitutions, which are single character mis-matches, are penalized 1 unit
Insertions/Deletions (“indels”), which create gaps, are penalized 5 units
Matches are rewarded -3 units
Make your pseudo-code easy to follow, but keep it within one page. If needed for clarity, document your algorithm with legible comments in important places in the pseudo-code. Clear pseudo-code provides evidence of your comprehension. The correctness of your approach should be easy for the reader (e.g., TA) to verify. If the TA cannot easily determine the code's correctness, then fewer points will be awarded.
Implement the scoring algorithm. When scoring, only align the first 5000 characters (bases) of each sequence. Implement your algorithm in the PairWiseAlign.Align() method. That method should return the alignment score.
Document your algorithm with legible comments in important places in the code that make it obvious to the reader what your solution is doing. This documentation also provides evidence of your comprehension. With the aid of adequate documentation, the correctness of your approach should be easy for the reader (e.g., TA) to verify. If the TA cannot easily determine the code's correctness, then fewer points will be awarded.
Record the pair-wise scores computed by the scoring algorithm in the given 10×10 score matrix such that position (i, j) in the display shows the optimal distance from sequencei to sequencej for the first 5000 characters. Since the matrix is symmetric, you should only fill the upper part of the matrix (above the diagonal). Correctness of your algorithm will be checked using this matrix. (There is also no need to fill the diagonal, since the alignment of a sequence with itself consists only of matches.)
As an aid to debugging, the first two sequences in the database are the strings: “polynomial” and “exponential”. The string “polynomial” is the sequence for the first row (and column) of the score matrix, and “exponential” comes second. While these strings aren’t biologically valid DNA sequences, they are the strings used in an example in the textbook.
To help you verify the correctness of your algorithm, with our operator costs the optimal alignment of these two strings should be -1 (your code should compute that result for the cell at row 1 and column 2 in the table).
You could also try the operator costs in the book chapter and verify your DP table against the one in the book (see pp. 163-164 in the print textbook).
As a further aid for verifying the correctness of your algorithm, here is another value that should appear in your table: (counting from 1) at row 3, column 4, the result should be -14972. That is the result of aligning the first 5000 bases each of the genomes for “Bovine coronavirus isolate BCoV-LUN” and “Bovine coronavirus isolate BCoV-ENT”.
Implement the extraction algorithm. Your function should produce a character-by-character alignment of its two sequence arguments. (This function should not be called to fill the score matrix.)
Add a text field to your GUI for displaying an extracted alignment. (Right click on MainForm.cs in the “Solution Explorer”, and choose “View Designer” to view the GUI in designer mode and gain access to the toolbox of visual controls.)
Add a click event to the GUI table cells. The method handling this event should use your extraction algorithm to calculate the optimal alignment for the strings corresponding to that cell and should display the alignment in the text field. Thus, the field will be updated whenever you click on a cell in the score table.
To add the click event, select the DataGridView (the gray box in the middle of the main form), and select the Events tab (the lightning bolt) on the Properties list. Add a handler for CellMouseClick by double clicking on its row.
Display the alignment in a manner that easily reveals the matches, substitutions, and insertions/deletions (indels), such as is shown in the short example below. Gaps should be shown with a '-' (hyphen).
Extract and display the alignment of the first 100 characters (bases) (no more, no less) of each of the selected sequences in the pair. (The alignment itself will most likely include gaps and will therefore be longer than 100 characters.)
In case there is more than one optimal alignment, choose one of them.
For the extra mile, display all of the optimal alignments.
Align the first 100 characters (bases) of sequence #3 (row 3) and #10 (column 10) (assuming the first sequence in the table is numbered as #1); extract and display the alignment in your report using a fixed-width font. For example, if you were aligning “AGCTCATGCT” and “ACTGCATCA”, the side-by-side alignment should be presented in the manner shown here:
AGCT-CATGCT
A-CTGCAT-CA

#####Demonstration
*Now we show a shiny version of the project to see the algorithm in action. Yay for coming to the help session! If you aren't here and there is enough interest, I can add some screen shots to these notes later. See the `More Info` section for how to contact us to demonstrate your interest.*

#####More Info

Always check the syllabus, project specs for help, try searching Google, then the Google Group for the class, and finally we are available through the TA Email, our office hours, and by appointment. Preferably in that order.

###Questions?
