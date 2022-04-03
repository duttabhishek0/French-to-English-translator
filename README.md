# French-to-English-translator
Nerual Model to translate French text to English Text
## Model used : LSTM-based se2seq

### Dataset Used = http://www.manythings.org/anki/fra-eng.zip


> The project can be seen more as a pattern matching project, rather than a ML project. xD
<br>

The code is divided into following parts:

1. Data-Cleaning and Pre-processing(The Major Part)
2. Creating a tokenizer

    i. English Tokenizer
    
    ii. French Tokenizer
3. Encoding sequence to Integers(One Hot Encoding)
4. Building the model


### 1. Data Cleaning and Pre-Processing

<p align="center">
    <img src="https://user-images.githubusercontent.com/56694152/161415269-8bbb09a3-2200-4acb-8bf6-2303e7e18ca2.jpg" width="490" height="500">
</p>

### 2. Creating a tokenier

#### English Tokenizer
<p align="center">
    <img src="https://user-images.githubusercontent.com/56694152/161415411-9da90169-a96d-422e-98da-742f61ba12e6.png" width="600" height="200">
</p>



#### French Tokenizer

<p align="center">
    <img src="https://user-images.githubusercontent.com/56694152/161415468-f5cc90d9-41fe-4587-b853-cd4ee3913343.png" width="600" height="200">
</p>

### Fitting the model
#### Batc Size : 25
#### Epochs : 50


### Metrics:

For checking the model, **BLEU scoring** is used:

Evaluation involves two steps:

1.Generating a translated output sequence, followed by

2.Repeating this process for many input examples and summarizing the skill of the model across multiple cases.

#### Score : 93%(Training)   84(Testing)

### Example : 

| Source             | Target        | Predicted      |
| ------------------ | ------------- | ---------------|
| jadore les enigmes | i love puzzles| i love puzzles |
| jai ete secouee    | i was shaken  | i was attacked |
| ils sont pieges    | theyre trapped| theyre trapped |
| quand cela sestil termine | when did it end |when does it end |
| ne touche pas a ceci | dont touch this  |dont touch that
|
