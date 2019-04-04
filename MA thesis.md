# A Corpus-Based, Comparative Analysis of Professional and Amateur Literary Style

-----

In my MA thesis, I want to compare amateur and professional (or *award-winning*, to be more precise) science-fiction novels in order to establish a set of relatively objective “guidelines” for amateur writers who want to improve their writing and achieve higher critical acclaim and commercial success. Therefore, the aim of my paper is to explore the realm of literary stylistics with the use of methods characteristic for corpus linguistics. Such a blend of language studies is often referred to as ***corpus stylistics*** and is, relatively speaking, quite an unexplored area in linguistics.

Since the emergence of computers, there has been a heated debate about whether literature may be analysed quantitatively which, for the most part, entails emphasis on syntax and grammar and not the semantics of a given piece of text. Many traditionalists believe that, because of the very nature of literature, it cannot be analysed in a non-subjective way, as it assumes its final form in readers’ minds. This cognitive approach calls into question all of corpus linguistics’ relevance.

Some linguists, however,  believe that the corpus-based approach can be incredibly useful for pursuing a great number of literary questions. It proves to be particularly useful for purposes connected with stylometry (i.e. identifying the author of a given text or simply estimating when it was written) and overall analysis of style, because as such, it does not crystallize in reader’s mind; its form is very clear and objective on pages of a book.

The very **concept of style**, however, is an elusive one and its definition vary greatly. In traditional linguistics, style is simply defined as choice, i.e. how the speaker chooses to convey given message (he may, for example, choose a formal register). This definition is not particularly useful for corpus stylistics and is widely ignored. Instead, there are two main other definitions of style which apply here:

1. First of, we have **style as recurrence**. This definition is mostly taken into account when we want to use corpus linguistics as a means of providing substantiation for literary claims. This approach reveals all of the patterns in a text which can be used to validate and elaborate on existing theories of literature. For example, if we analyse Jane Austen's *Northanger Abbey*, we can see that the most common 4-grams (fixed collocations of 4 words) are delexicalised discourse markers in direct speech, which not only confirms that her characters are superficial, but also provides additional insight into how they are constructed.

2. Second definition is **style as deviation from norm**. This is extremely useful not only for attribution of authorship which was mentioned above, but also for describing author's idiolect, i.e. his way of writing (which would constitute the most intuitive definition of style).

In my paper, *both* of these definitions will be accepted, as both of them can help establish differences and similarities in professional and amateur writing. The number one priority is to analyse syntax and grammar (as to, for example, see what kind of grammatical patterns and types of sentence structure are most common), but if this topic will be exhausted too early, I will move on to study other stylistics questions such as what thematic groups are the most common, how the characters are constructed, or how emotionally charged the text are.

My research requires creation of three corpora:

| Name  | Description |
| ------------- | ------------- |
| ***The professional, award-winning corpus.*** | It will consist of around 20 books which were either nominated for or won one of the major science-fiction awards (*Nebula* and *Hugo Awards*) in the last 10 years.|
| ***The amateur, unpublished corpus.***  | This  corpus will consist of around 20 books written by amateur writers who have not published any texts in their lives. They will be taken from a website called Wattpad and will be chosen based on their popularity among users. |
| ***The science-fiction reference corpus.***  | For the purpose of putting all analyses in context, I will also need a much bigger corpus which will help me establish genre conventions and average style parameters of a science-fiction writer. This corpus will consist of a random selection of 100 science-fiction books published in the last 20 years. It is a necessary step for analysing style as deviation from norm.|


For the purpose of extracting and processing linguistics data, I will mostly use the **NTLK library for Python**, as it seems to be the most versatile and flexible tool available, but I will also most certainly refer to a number of other sources, such as the WebSty tool created by the Clarin-PL team.

Here is a piece of code which I will use for part-of-speech tagging:

```python
import nltk 
from nltk.corpus import stopwords 
from nltk.tokenize import word_tokenize, sent_tokenize 
stop_words = set(stopwords.words('english')) 
  
// Dummy text 
txt = "Lorem ipsum dolor sit amet, consectetur adipiscing elit. Etiam interdum malesuada varius. Vestibulum sit amet lectus turpis.  Nunc ac auctor augue, eu tincidunt augue. Aenean commodo et libero a ultricies. Curabitur tempus dignissim bibendum.  Nullam at mi sed massa convallis pretium eu non purus. Aliquam a diam sed nunc venenatis lacinia.  Suspendisse dignissim nec felis eget sodales. Nunc luctus lectus nisl. Nunc fermentum porta varius."
  
tokenized = sent_tokenize(txt) 

for i in tokenized: 
    wordsList = nltk.word_tokenize(i) 
    wordsList = [w for w in wordsList if not w in stop_words]  
    tagged = nltk.pos_tag(wordsList) 
  
    print(tagged) 
```

If my analysis yields satisfying results, at the very end I will create a set of guidelines (not *rules*) for amateur writers who want to improve their writing. This may serve as an alternative for attending creative-writing classes which also aim to improve the style of writing of participants.

If not, I will be able to conclude that the application of corpus linguistics in stylistics has major restrictions and little can be concluded from an almost completely objective analysis of style. ~~Let’s hope that doesn't happen.~~
