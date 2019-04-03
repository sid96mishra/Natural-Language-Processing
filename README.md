# Natural-Language-Processing

Analysis of Free Text and Natural Language Processing.

In this project authorship of the FEDERALIST essays known as The Disputed Papers were analysed.

## Disputed Papers

The Federalist Papers were written in 1787-1788 by Alexander Hamilton, John Jay and James Madison to persuade the citizens of the State of New York to ratify the U.S. Constitution. As was common in those days, these 77 shorts essays, about 900 to 3500 words in length, appeared in newspapers signed with a pseudonym, in this instance, “Publius”. In 1778 these papers were collected along with eight additional articles in the same subject and were published in book form. Since then, the consensus has been that John Jay was the sole author of five of a total 85 papers, that Hamilton was the sole author of 51, that Madison was the sole author of 14, and that Madison and Hamilton collaborated on another three. The authorship of the remaining 12 papers has been in dispute; these papers are usually referred to as the disputed papers. It has been generally agreed that the disputed papers were written by either Madison or Hamilton, but there was no consensus about which were written by Hamilton and which by Madison.

The authorship of seventy-three of The Federalist essays is fairly certain. Twelve of these essays are disputed over by some scholars, though the modern consensus is that Madison wrote essays Nos. 49–58, with Nos. 18–20 being products of a collaboration between him and Hamilton; No. 64 was by John Jay. The first open designation of which essay belonged to whom was provided by Hamilton who, in the days before his ultimately fatal gun duel with Aaron Burr, provided his lawyer with a list detailing the author of each number. This list credited Hamilton with a full sixty-three of the essays (three of those being jointly written with Madison), almost three-quarters of the whole, and was used as the basis for an 1810 printing that was the first to make specific attribution for the essays. 

Madison did not immediately dispute Hamilton's list, but provided his own list for the 1818 Gideon edition of The Federalist. Madison claimed twenty-nine numbers for himself, and he suggested that the difference between the two lists was "owing doubtless to the hurry in which (Hamilton's) memorandum was made out“. A known error in Hamilton's list was Hamilton incorrectly ascribed No. 54 to John Jay, when in fact, Jay wrote No. 64.

## Course of Action
- Dataset containing 85 essays was loaded and cleaned. 
- TFIDF matrix of the corpus was created. 
- Cosine Similarities were computed between all pairs of essays. 
- Hamilton incorrectly ascribed No. 54 to John Jay, when in fact, Jay wrote No. 64. 
- Used 3-gram language model to analyse potential authorship of the unknown Federalist Papers. Specifically, we compute the average cosine similarity between all the known Hamilton papers and all the unknown papers (and similarly between known Madison and unknown, and Jay and unknown). 
- We also analysed the similarity between Jay's papers and paper No. 54 and No. 64 to check which one of the two is more likely to be written by John Jay. 
- Finally, we used our language model to generate text. Analysis was done without the use of any language processing python libraries.

## Conclusion

We clearly observe that there is a very high chance that Jay has written paper 64 compared to paper 54. Also, there is high possibility that unknown papers were written by Madison.

Perplexity values of our 3-gram language model with Hamiltonian papers and non-Hamiltonian papers:

- Average Perplexity of Hamilton Language Model on papers written by Hamilton :12.572999895650277 
- Average Perplexity of Hamilton Language Model on papers not written by Hamilton :1792.80849782821  

We clearly observe that the perplexity of papers written by Hamilton have lesser perplexity than other which indicates that our Language Model works properly. 
