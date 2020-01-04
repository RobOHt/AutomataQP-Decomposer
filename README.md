# Automata Question Paper Decomposer
AutomataQP Decomposer is a python program that automatically decomposes an Automata paper
into separate questions. 

## Run program

The project runs on Python 3.

1. Make sure that the pdf format question papers intended for decomposition are ready in 
folder `papers`. Make sure that all folder or files with `SAMPLE_...` name are removed.

2. Run `decomposer.py` in terminal

3. Outputs will be stored in a json file and sqlite3 database.

4.  - The database consists of a table with 5 columns: the image, and choices A-D.
	- The image is a photo of the entire question. It can be used for supplementary role 
	if the text version choices are of unsatisfactory quality. 
	- There may be no text record for some questions. This is because this program simply
	couldn't OCR this question after three OCR attempts, each time with a different image
	enhancement level.

5. The json file stores similar contents to that of the database, except that questions
are stored as such: 

	[[`question-xxxxxx.png`, [`(A)Question A.`, `(B)Question B.`, `(C)Question C.`, `(D)Question D.`]]
	...
	]