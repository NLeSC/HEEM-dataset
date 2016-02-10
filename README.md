# HEEM-dataset

* guidelines (in Dutch)
* DONE human annotated data ( NAF)
* DONE machine annotated data (NAF)
* lexicon based on annotated data (LMF)
* overview annotation tags, and emotion hierarchies
* + korte beschrijving per dataset
* data license
* Translation between Dutch and English labels
* Corpus metadata?

The dataset consists of four subsets:

1. Annotation corpus: texts selected from
[Nederlab](http://www.nederlab.nl/) manually annotaded with HEEM labels
(including humor modifiers and intensifiers) (29 texts)
2. Ceneton: texts selected from [Ceneton](http://www.let.leidenuniv.nl/Dutch/Ceneton/) (34 texts)
3. Corpus big: other texts selected from
[Nederlab](http://www.nederlab.nl/) (149 texts)
4. EDBO: texts selected from [Early Dutch Books
Online](http://www.earlydutchbooksonline.nl/en/edbo) (67 texts)

## naf

The `naf` directory contains the annotations and predicted labels in NAF-
format. The emotions can be found in the emotions-layer:

```xml
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

## lexicon

The `naf` directory contains the annotations and predicted labels in NAF-
format. The emotions can be found in the emotions-layer:

```xml
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

## lexicon
```
  The lexicon contains all wordforms from the manually annotated corpus, 
  their concepttypes (i.e. Emotion, Bodypart, Bodily process 
  or Emotional Action) and the emotion(s) they evoke. The lexical data
  are represented in xml following the guidelines from the Lexical Markup Framework.
```
