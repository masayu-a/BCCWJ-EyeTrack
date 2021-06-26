# BCCWJ-EyeTrack

## Description
EyeTracking data (24 Japanese Native Speakers) on BCCWJ Newspaper Samples

## Features


## Author
Masayuki Asahara (National Institute for Japanese Language and Linguistics, Japan)

## Packager
Masayuki Asahara (National Institute for Japanese Language and Linguistics, Japan)

## License 
CC BY-NC-SA 3.0
https://creativecommons.org/licenses/by-nc-sa/3.0/deed.ja

## Credit
National Institute for Japanese Language and Linguistics (2018)
`BCCWJ-EyeTrack' (ver. 1.0.0)

## Data format

the files without the original text for Stan analysis

### filenames

- fft: First Fixation time
- fpt: First Pass Time
- spt: Secound Pass Time
- rpt: Regression Path Time
- total: Total Time
- self: Self paced reading Time

### {fft,fpt,spt,rpt,total,self}.csv or {fft,fpt,spt,rpt,total,self}-del.csv

{fft,fpt,spt,rpt,total,self}.csv files include titles, subtitles, lists, and captions.

{fft,fpt,spt,rpt,total,self}-def.csv files exclude titles, subtitles, lists, and captions.

### the columns

- logtime: (logarithmic values (log(x)) of fixation/reading time)
- invtime: (reciprocal values (1/x) of fixation/reading time)
- surface: the original text masked by "_" due to the copyright issue
- time: fixation/reading time (msec)
- measure: (fft, fpt, spt, rpt, total or self)
- sample: sample id (A, B, C, D)
- article: article id in BCCWJ
- metadata_orig: (the BCCWJ original metadata categories of titles, subtitles, lists, captions, texts, and so on.)
- metadata: the modified version of the metadata categories of titles, subtitles, lists, captions, texts, and so on.
- sessionN: session order
- length: length of the surface, namely the number of characters in the original text
- space: presented with or without spaced between the phrases
- subj: subject participant id
- setorder: (the presentation order for the subject participants)
- rspan: the subject feature -- the result of reading span test
- voc: the subject feature -- the result of vocab test
- dependent: the number of the dependent for the phrase
- articleN: article presentation order
- screenN: screen presentation order
- lineN: line presentation order -- the vertical offset
- segmentN: segment presentation order -- the horizontal segment order in the line
- sample_screen: (screen id)
- is_first: is_first segment in the line (1: FALSE, 2: TRUE)
- is_last: is_last segment in the line (1: FALSE, 2: TRUE)
- is_second_last: is_last segment in the line (1: FALSE, 2: TRUE)
- infostatus, definiteness, specificity, animacy, sentience, agentivity, commonness:
  the annotation of the information structure from BCCWJ-InfoStr
- CLRHST, CLRMST, CLRFUT, CLRHRT, CLRHSL, CLRMSL, CLRFUL, CLRHRL, CLMHST, CLMMST, CLMFUT, CLMHRT, CLMHSL, CLMMSL, CLMFUL, CLMHRL:
  the annotation of the clause boundary infomation from BCCWJ-ToriClause
- WLSPSUWA, WLSPSUWB, WLSPSUWC, WLSPSUWD, WLSPLUWA, WLSPLUWB, WLSPLUWC, WLSPLUWD:
  the annotation of the thesaurus categories from BCCWJ-WLSP
- cbow_norm, cbow_prev, skip_norm, skip_prev:
  word embedding features from NWJC2vec -- Japanese Word Embeddings
- count, count_ave, count_log, count_ave_log, count_ave_kika:
  word frequency features from NINJAL Web Japanese Corpus
- bid, did:
  word dependency information from BCCWJ-DepPara
  we used `dependent' column for analysis
- type_pred, dist_invga, type_ga, dist_invo, type_o, dist_invni, type_ni:
  predicate argument relation from BCCWJ-PAS

### {fft,fpt,spt,rpt,total,self}.tbl

these files includes the annotation data
- 0th column
  the number of column in *.csv
- 1st column
  the label of annotation data
- 2nd column
  the id in *.csv

## Contact
masayu-a -at- ninjal.ac.jp