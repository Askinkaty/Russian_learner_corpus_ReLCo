# Russian learner corpus
Corpus of errors collected automatically by [Revita language learning system](http://revita.cs.helsinki.fi/)


*NEW DATA ADDED:*

File `phrases_with_annotation.txt` includes short paragraphs in Conll format 
with manually annotated answers from language learners of Revita.
Format of the data: 

* The learner answers in the first column.
* If an answer is different from the original word in the sentence, 
 second column has a replaced word, otherwise -- None.
* Third column: Err mark errors, MA -- grammatically acceptable answers.
* The last column: 0 label for errors, 1 -- for grammatically correct words.
  
  
The file includes 3004 paragraphs with on average 2 sentences per paragraph.
________


The directory `automatically_extracted_errors` contains several files with annotated errors from Revita Learner Corpus (ReLC)

* `gram_err.csv` - file with grammatical errors (an answer given by the learner has the same lemma as the expected answer, so they are forms from the same paradigm);
* `nonword_err.csv` - file with errors which do not exist in the dictionary (spelling errors);
* `wronglemma_err.csv` - file with error which lemma is different from the lemma of the expected answer.

Files starting with 'correct' have correct forms in the same sentences (also marker by undescores).
All these files were automatically annotated.

Every file has the following columns: 
* learner's id; 
* time when error was made;
* attempt (the system provides currently 2 attemps to practice the same exercise);
* sentence with errors marked by undescores ;

File `annotated_sent.csv` is a file with manual annotation. New columns here are 'label' and 'category'.

Labels:
- 0: grammatical error;
- 1: correct answer;
- 2: pragmatic error;
- 3: broken or context is not enough to annotate;
- 4: non-word error;
- 7: other.

Category includes more detailed information about the given asnwer -- how is it different from the expected answer. 
For example, tag 'Tense: fut/past, Number: s/p' means that an answer is in the future tense and singular number, but the expected answer is plural past tense verb. 

IN PROGRESS: 
All sentences are morphologically annotated, this addidional data will be added to all files.

For details and questions, contact: anisia.katinskaia@helsinki.fi
