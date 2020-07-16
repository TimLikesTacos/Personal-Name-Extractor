This was a project for school.  Since this project may be used in future semesters, only item available in this repository is the final jar file is available.  
If you are not a student working on a similar project, and want to review the source code, message me and I can provide.

# Personal Name Extractor (PNE)
The purpose of the Personal Name Extractor (PNE) is to explore the option of replacing standard coded methods of name extraction with a solution based on learning machines.

Using machine learning,  the PNE will examine text from the opening pages of a document in order to extract personal names. Machine learning will be used as the Extract project had found that identifying names by hard-coded function was challenging and were overwhelmed by coding in exceptions and altering rules. These exceptions included rules for last-name-first, or professional titles such as “Dr.” or military ranks like “Lt.”. With machine learning, the system will be trained using supplied information to identify all the different ways a personal name can appear in a document.


The project provides library that can be embedded within Extract or other similar metadata collection projects.

All identified names are surrounded with \<PER> tags. For example:
>"\<PER>George Washington\</PER> was the first president of the United States"

## Use
### Extractor
For the developer using the library, a `String` of marked names can be obtained by entering a `String` containing text to be identified into the `static` method `Extractor.markPersonalNames (String)`.
For example:
>```java
>String marked = Extractor.markPersonalNames("Aryton Senna was from Brazil");
>System.out.println(marked);
>```
Output:
>`"<PER>Aryton Senna<PER> was from Brazil"`

### Jar File
The project also comes with an executable .jar file that reads from the standard input and standard output.   This can be used for reading text files.
If the input text file has blocks of text separated by \<NER> tags, then these blocks will be processed individually. 
>`java -jar Librarian.jar < input.txt > output.txt`

