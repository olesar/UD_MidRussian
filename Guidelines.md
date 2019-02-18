### Introduction

Middle Russian Corpus (MidRus) is part of the Russian National Corpus (http://ruscorpora.ru) included in the collection of historical corpora (Sichinava 2014). 
The annotation of MidRus takes into account the research interests of the following users:  
* researchers in the Middle Russian period of the language  
* researchers of the Old Russian languages accustomed to the schema ot the RNC Old Russian corpus (OldRus)  
* researchers of the Modern Russian language interested in the micro-diachrony studies. They are accustomed to the schema ot the RNC Main corpus  
* NLP researchers who would like to use the Middle Russian data in their computational experiments, including comparative ones based on various paleoslavic data collections.  

To meet these, somewhat different, demands, a number of specifications are considered to facilitate necessary data linking and conversion.  

The morphological annotation standard of MidRus adopts two schemas (tagsets) in parallel:
* RNC-MidRus: RNC Middle Russian tagset close to those of the RNC Main corpus and the RNC Old Russian corpus  
* UD-MidRus: Universal Dependencies tagset close to those of the UD-Church Slavic and UD-Russian data collections.  

The conversion table between RNC and UD tags is provided here: [MidRussianUD.md](https://github.com/olesar/UD_MidRussian/MidRussianUD.md).  


### Analytical forms  

The analytical forms are annotated as two (or more) tokens cross-linked at the morphological (cf. OldRus) and syntactic (UD) level. All tokens are labeled `analyt` (UD: Analyt=Yes), the grammatical features are labeled on the token in which the category is expressed:  

(1)
\[RNC-MidRus\]
```
а       <ana lex="а" gr="CONJ"></ana>
будет   <ana lex="быти" gr="V,3p,act,analyt,fut2,indic,intran,sg" gr_ext="IN:FUT2+3312"></ana>
не      <ana lex="не" gr="PART"></ana>
дошла   <ana lex="доити" gr="V,act,f,intran,perf,pf,sg" gr_ext="IN:FUT2+3310"></ana>
```

\[UD-MidRus\]
```
1 а       а     CCONJ _ _                                                               4 cc
2 будет   быти	AUX 	_ Analyt=Yes|Mood=Ind|Number=Sing|Person=3|Tense=Fut2|Voice=Act   4 aux
3 не      не	  PART  _ Polarity=Neg                                                    4 advmod
4 дошла   доити	VERB	_ Analyt=Yes|Aspect=Perf|Gender=Fem|Number=Sing|Tense=Past|
                        Transit=Tran|VerbForm=PartRes|Voice=Act                         0 root
```

In example (1), number and person is labeled on the auxiliary _будет_, and gender, number is labeled on the content verb _дошла_. The content verb is also labeled as `perf` (UD: Tense=Past, VerbForm=PartRes) whereas the auxiliary is labeled by the tense of the whole analytical form `fut2` (UD: Tense=Fut2). Furthermore, _будет_ is labeled as `AUX` (part of speech) and `aux` (dependency relation) in UD.


