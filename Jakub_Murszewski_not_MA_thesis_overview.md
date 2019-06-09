![CoverImage][Cover]

# Introduction


Simple Sentiment Analysis Tool (SSAT) is a tool dedicated to performing a sentiment analysis with the use of statistical examination upon a text.

## Features


* Determinig the number and percentage of the positive, negative and neutral tokens in the text;
* Determinig the number and percentage of the positive, negative and neutral tokens in the text, with the automatic deletion of stopwords in the text;
* Searching for keywords in the text and analysing only the sentences containing them;
* Automatically viewing the data, both as text and graphs;
* Saving the extracted data to a file

# Before you start


SSAT's script is written in Python 3 programming language and as such requires Python 3 installed on the computer. Moreover, the programme requires several Python 3 modules, namely:
* MatPlotLib
* Re
* Collections

Those need to be installed before using SSAT.

# Installation


Simple Sentiment Analysis Tool does not need installing. The software can be opened via the console or any Python interpreter.

For the programme to work correctly, several additional files need to be present. Those are:

* *.txt* file with negative sentiment words
* *.txt* file with positive sentiment words
* *.txt* file with stopwords

All of which need to be located in the same folder as the main programme file.

**The code and necessary .txt files can be downloaded from:**

[Here](https://github.com/MurszewskiJ/SSAT)

# User Guide


**First thing to appear after opening the program is the following menu:**

![Menu][Menu]

To access one of the functions of SSAT enter the number associated wit the function and press *ENTER*

### Functions


**"1. Sentiment Analysis (with stopwords)"**


This function will analyse the whole selected text without deleting any of its contents.

Upon selection of this option, the following will appear:

![image_1][image_1]

To proceed, enter:
* either the path to the file which you want to analyse (if the file is not in the same folder as the programme
* or only the name of the file (if the file is in the same folder as the programme)


**Note that the file you wish to analyse should be in .txt format.**

Then, press *ENTER*.



The program will analyse the text and display the result (i.e. the overall sentiment of the text).

To see the details and charts, type "Y" in the following prompt:

![image_2][image_2]

Then, press *ENTER*.

Then, the programme will display the following:

* Percentage value of positive words
* Percentage value of negative words
* Percentage value of neutral words
* List of most common negative words
* List of most common positive words
* List of most common neutral words
* Chart containing the percentage value of the overall sentiment
* Chart with the most common positive words (up to 10)
* Chart with the most common negative words (up to 10)
* Chart with the most common neutral words (up to 10)

To save this data to a file, type "Y" in the following prompt:

![image_3][image_3]

Then, press *ENTER*.

Then, enter the name of the file in the following prompt:

![image_4][image_4]

**The name of the file should end with _".txt"_.**

Then, press *ENTER.*

The programme will then proceed to save the data to the following file, which will be then localised in the same folder as the programme.

**"2. Sentiment Analysis (without stopwords)"**

This function will analyse the selected text after deleting stopwords from it.

This function shares its operations with the previous function. For a step-by-step guide, see **"1. Sentiment Analysis (with stopwords)"**.



**"3.Keywords Analysis (with stopwords)"**

This function will search the text for sentences with the chosen keyword.

Upon selecting this option, the following will appear:

![image_5][image_5]

To proceed, enter tke keyword you wish to search for.

**Remember that it is case sensitive.**

Then, press *ENTER*.

Next, the following will appear:

![image_1_2][image_1]

To proceed, enter:
* either the path to the file which you want to analyse (if the file is not in the same folder as the programme
* or only the name of the file (if the file is in the same folder as the programme)


**Note that the file you wish to analyse should be in .txt format.**

Then, press *ENTER*.

The programme will then display the list of sentences in which the keyword appears.



To view the analysed sentiment of the sentences, type "Y" in the following prompt:

![image_6][image_6]

The program will analyse the text and display the result (i.e. the overall sentiment of the text).

To see the details and charts, type "Y" in the following prompt:

![image_2_2][image_2]

Then, press *ENTER*.

Then, the programme will display the following:

* Percentage value of positive words
* Percentage value of negative words
* Percentage value of neutral words
* List of most common negative words
* List of most common positive words
* List of most common neutral words
* Chart containing the percentage value of the overall sentiment
* Chart with the most common positive words (up to 10)
* Chart with the most common negative words (up to 10)
* Chart with the most common neutral words (up to 10)

To save this data to a file, type "Y" in the following prompt:

![image_3_2][image_3]

Then, press *ENTER*.

Then, enter the name of the file in the following prompt:

![image_4_2][image_4]

**The name of the file should end with _".txt"_.**

Then, press *ENTER.*

The programme will then proceed to save the data to the following file, which will be then localised in the same folder as the programme.

**"4.Keywords Analysis (without stopwords)"**

This function will search for the sentences containing a chosen keyword , then analyse the text after deleting stopwords from it.

This function shares its operations with the previous function. For a step-by-step guide, see **"3.Keywords Analysis (with stopwords)"**.

# Altering Files

It is possible to add and remove elements form the files containing lists of negative or positive sentiment words and stopwords.

### Removing Elements from the Lists

To remove an element form a list:
* Open one of the following files:
    * positive_words.txt
    * negative_words.txt
    * stoplist.txt
* Remove the line of text containing the word you wish to delete
* Save changes to the file

### Adding Elements to the Lists

To add an element to the list:

To remove an element form a list:
* Open one of the following files:
    * positive_words.txt
    * negative_words.txt
    * stoplist.txt
* In a new line, enter the word you wish to add
* Save changes to the file






[Cover]: https://i.ibb.co/7CXJDtC/Titlepage.jpg
[Menu]: https://i.ibb.co/cJxnN4J/0.jpg
[image_1]: https://i.ibb.co/H7bjPbH/1-1-1.jpg
[image_2]: https://i.ibb.co/23gsjP9/1-2.jpg
[image_3]: https://i.ibb.co/dK3FNLD/1-3.jpg
[image_4]: https://i.ibb.co/r3cch19/1-4.jpg
[image_5]: https://i.ibb.co/mtGCTdb/3-1-1.jpg
[image_6]: https://i.ibb.co/c1nSj9N/3-2.jpg
