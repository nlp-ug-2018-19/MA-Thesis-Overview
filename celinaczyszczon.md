#### _Celina Czyszczoń MA Thesis Plan_
## Sentiment Analysis of _Black Mirror_ Netflix TV Series

In my MA I am going to focus on analysing sentiment of larger samples of data such as episodes of TV series. I have decided to compile a corpus consisting of the transcripts of Black Mirror episodes, as they are renowned for their depressing character. 

## *Plan*
1. Theory
   1. Corpus Linguistics
   2. Axiology
   3. Moderated discourse
   4. Construction grammar
   4. Discourse analysis
   5. Sentiment analysis
2. Research
    1. Sentiment analysis of the series using a simple lexicon-based tool vs more sophisticated Vader Sentiment tool
    2. Emotions in the TV series - an analysis based on Martindale's dictionary 
    
    
## Chapter 1
   The first chapter of my thesis focuses on using corpora in linguistic research. Firstly, it defines the notion of a corpus, explains how a corpus can be compiled and provides examples of general corpora that are available on-line. Then, it discusses the practical applications of corpora in computational linguistics. Finally, the chapter presents corpus linguistics as a methodology employed by researches of many different fields of linguistics and shortly discusses its advantages and limitations. 
   
## Tools for research 
#### VADER
   I plan on relying my research mostly on VADER (Valence Aware Dictionary and sEntiment Reasoner), which is a lexicon and rule-based sentiment analysis tool available [here](https://github.com/cjhutto/vaderSentiment)
   
   example of code:

      S04E02 = S04E02.split('\n')
      from vaderSentiment.vaderSentiment import SentimentIntensityAnalyzer
      analyzer = SentimentIntensityAnalyzer()
      for sentence in S04E02:
          pol = analyzer.polarity_scores(sentence)['compound']
          if pol != 0:
              vs = analyzer.polarity_scores(sentence)
              print("{:-<65} {}".format(sentence, str(vs)))
              
   sample output: 
   
         OK. All set, then.----------------------------------------------- {'neg': 0.0, 'neu': 0.506, 'pos': 0.494, 'compound': 0.4466}
         incision. Hand me the Bovie.------------------------------------- {'neg': 0.0, 'neu': 0.556, 'pos': 0.444, 'compound': 0.4939}
         ridiculous. Don't apologize.------------------------------------- {'neg': 0.791, 'neu': 0.209, 'pos': 0.0, 'compound': -0.4207}
         - Hey, it's gonna be fine.--------------------------------------- {'neg': 0.0, 'neu': 0.69, 'pos': 0.31, 'compound': 0.2023}
         you want to hold my hand.---------------------------------------- {'neg': 0.0, 'neu': 0.471, 'pos': 0.529, 'compound': 0.5423}
         OK, we're ready-------------------------------------------------- {'neg': 0.0, 'neu': 0.155, 'pos': 0.845, 'compound': 0.6633}
         now. How are the vitals?----------------------------------------- {'neg': 0.0, 'neu': 0.656, 'pos': 0.344, 'compound': 0.2732}
         Still good. You're----------------------------------------------- {'neg': 0.0, 'neu': 0.408, 'pos': 0.592, 'compound': 0.4404}
         gonna feel a little pressure now.-------------------------------- {'neg': 0.323, 'neu': 0.677, 'pos': 0.0, 'compound': -0.228}
         Cutting the umbilical cord.-------------------------------------- {'neg': 0.333, 'neu': 0.667, 'pos': 0.0, 'compound': -0.128}
         Is she OK?------------------------------------------------------- {'neg': 0.0, 'neu': 0.405, 'pos': 0.595, 'compound': 0.4466}
         - Say she's OK.-------------------------------------------------- {'neg': 0.0, 'neu': 0.405, 'pos': 0.595, 'compound': 0.4466}
         - Hey, hey, hey. It's OK.---------------------------------------- {'neg': 0.0, 'neu': 0.577, 'pos': 0.423, 'compound': 0.4466}
         Oh, God! Oh, God...---------------------------------------------- {'neg': 0.0, 'neu': 0.556, 'pos': 0.444, 'compound': 0.3382}
         - Is she OK?----------------------------------------------------- {'neg': 0.0, 'neu': 0.405, 'pos': 0.595, 'compound': 0.4466}
         - Just relax. Hold on. OK?--------------------------------------- {'neg': 0.0, 'neu': 0.34, 'pos': 0.66, 'compound': 0.7034}
         Good job.-------------------------------------------------------- {'neg': 0.0, 'neu': 0.256, 'pos': 0.744, 'compound': 0.4404}
         She's great.----------------------------------------------------- {'neg': 0.0, 'neu': 0.196, 'pos': 0.804, 'compound': 0.6249}
         Oh, she's beautiful.--------------------------------------------- {'neg': 0.0, 'neu': 0.339, 'pos': 0.661, 'compound': 0.5994}

#### LBSA 
   I might compare the results of analysis using VADER with the results from a very simple tool, relying only on lists of positive and negative words. For this purpose I would use a python programme that I have developed with my coursemate Patrycja Brzezinska. [link](https://github.com/celinaczy/LBSA---Lexicon-Based-Sentiment-Analysis)

#### MARTINDALE'S REGRESSIVE IMAGERY DICTIONARY

   Possibly I will also write a script which will enable me to determine the emotions within a given text. Here I would use the regressive imagery dictionary created by Martindale. It provides a list of words corresponding to a particular emotion.

EMOTIONS|Examples
--------|--------
Positive Affect|Cheerful, enjoy, fun
Anxiety|Afraid, fear, phobic
Sadness|Depression, dissatisfied, lonely
Affection|Affectionate, marriage, sweetheart
Aggression|Angry, harsh, sarcasm
Expressive|Behavior	Art, dance, sing
Glory|Admirable, hero, royal

## Bibliography 

* B. Liu, Sentiment Analysis and Subjectivity, [in:] Handbook of Natural Language Processing, 2 ed., 2010.
* Corpus Encoding Standard. Retrieved June 8, 2019 from https://www.cs.vassar.edu/CES/CES1-0.html
* Corpus of Contemporary American English. Retrieved May 26, 2019 from https://www.english-corpora.org/coca/
* Dictionary definition. oxforddictionaries.com. Retrieved June 8, 2019 from https://en.oxforddictionaries.com/definition/dictionary
* Hutto C.J., Gilbert E., VADER: A Parsimonious Rule-based Model for Sentiment Analysis of Social Media Text, AAAI, 2014.
* Lindquist, H. (2009). Corpus Linguistics and the Description of English Edinburgh University Press Ltd
* McEnery, T., Wilson, A. (2001) Corpus Linguistics: An Introduction, 2nd ed. Edinburgh University Press Ltd
* Meyer, C. F. (2004). English Corpus Linguistics: An Introduction. Cambridge University Press 
* Stuart, K., Botella, A., Ferri, I. (2016) “A Corpus-Driven Approach to Sentiment Analysis of Patient Narratives” EPiC Series in Language and Linguistics 1, 381-395. Retrieved May 26, 2019 from https://easychair.org/publications/download/r8SR
* Taboada, M. , Sentiment Analysis: An Overview from Linguistics, Annual Review of Linguistics, 2016
* Wilkinson, M. (2006) Compiling Corpora for Use as Translation Resources. Retrieved 
* June 8, 2019 from https://translationjournal.net/journal/35corpus.htm
