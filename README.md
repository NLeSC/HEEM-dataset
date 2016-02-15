# HEEM-dataset

* DONE guidelines (in Dutch)
* DONE human annotated data ( NAF)
* DONE machine annotated data (NAF)
* DONE lexicon based on annotated data (LMF)
* DONE overview annotation tags, and emotion hierarchies
* DONE korte beschrijving per dataset (zie corpus metadata)
* data license
* DONE Translation between Dutch and English labels
* DONE Corpus metadata
* Link to naf (description of format)

The corpus consists of 279 texts.
Metadata about the corpus can be found in `corpus_metadata.csv` (please note that
  this is a **tab**-separated file). The metadata consists of:
* text id: file name of naf-files
* year: publication year of text
* genre: blijspel / komedie, klucht, tragedie/treurspel, Anders, unknown, Toneelspel, music
* title (for the ceneton texts this field is noisy and also contains other information
  such as the authors)
* authors: authors separated by & (also a noisy field)
* source: [nederlab](http://www.nederlab.nl/), [ceneton](http://www.let.leidenuniv.nl/Dutch/Ceneton/), or [edbo](http://www.earlydutchbooksonline.nl/en/edbo) (early Dutch books online)
* set: annotations/predictions
* period: classicism, renaissance, or enlightenment

## annotation guidelines
The annotation guidelines (Handleiding-annotaties-nl.pdf- version 2015) contain
* definitions of the HEEM concepts
* instructions on how to manually label emotions and bodyparts in the text

They are written in Dutch.

## labels
This directory contains JSON objects specifying mappings and clusterings.
* bodyParts: mapping between words for body parts used in the texts and body part categories (in English). For example, the words _hooft_, _kop_, and _hoofd_ belong to category **head**.
* HEEM clusters: clustering of HEEM labels into broader classes of emotions (see [1] for more details)
* PosNeg: clustering of  HEEM labels into 2 classes of emotions (postive and negative) (see [1] for more details)
* heemLabels and heemModifiers: translations of the Dutch HEEM labels and modifiers to English.
The English labels are used in the naf-files.

## lexicon
The lexicon contains the annotated words and multiword expressions from the manually annotated corpus,
their concepttypes (i.e. Emotion, Bodypart, Bodily process
or Emotional Action) and the emotion(s) they evoke. The data
is represented in xml following Lexical Markup Framework (LMF) guidelines which is the ISO standard for for Natural Language Processing (NLP) lexicons.

## naf
The `naf` directory contains the annotations and predicted labels in NAF-
format. The emotions can be found in the emotions-layer:

```
<emotions>
  <emotion id="emo0">
  <emotion_target/>
  <emotion_holder/>
  <emotion_expression/>
    <span>
      <!-- kop -->
      <target id="t1874"/>
    </span>
    <externalReferences>
      <externalRef reference="conceptType:bodyPart" resource="heem"/>
      <externalRef reference="head" resource="heem:bodyParts"/>
    </externalReferences>
  </emotion>
  <emotion id="emo1">
    <emotion_target/>
    <emotion_holder/>
    <emotion_expression/>
    <span>
      <!-- maek my de kop niet warm -->
      <target id="t1871"/>
      <target id="t1872"/>
      <target id="t1873"/>
      <target id="t1874"/>
      <target id="t1875"/>
      <target id="t1876"/>
    </span>
    <externalReferences>
      <externalRef reference="conceptType:bodilyProcess" resource="heem"/>
      <externalRef reference="emotionType:anger" resource="heem"/>
      <externalRef reference="anger" resource="heem:clusters"/>
      <externalRef reference="negative" resource="heem:posNeg"/>
    </externalReferences>
  </emotion>
</emotions>
```

## References

[1] J.M. van der Zwaan, I. Leemans, E. Kuijpers, and I. Maks. HEEM, a Complex
Model for Mining Emotions in Historical Text. 11th IEEE International Conference
on eScience, 2015 [10.1109/eScience.2015.18](http://dx.doi.org/10.1109/eScience.2015.18)
