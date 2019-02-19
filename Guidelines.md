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

We distinguish among the core annotation schema (RNC and UD), the extended schema (RNC-ext and UD-ext), and the simplified schema (UD-s used in comparative NLP experiments).  Unless otherwise stated, the guidelines will refer to the core annotation schema.  


### Part of speech tags and core grammatical tags

The lists of pos tags and core grammatical (inflectional) tags is available here: [MidRussianUD.md](https://github.com/olesar/UD_MidRussian/MidRussianUD.md). The document also report the mapping between the RNC and UD tags.  


### Parts of speech  

In general, the list of RNC can be mapped to the UD list almost straightforwardly, see the conversion table. `A`, `ANUM`, and the most part of `PRAEDIC` are mapped to `ADJ` (adjectives); `ADV`, `ADVPRO`, and `PARENTH` are mapped to `ADV` (adverb). `V` is splitted into `VERB` and `AUX`. `CONJ` is splitted into `CCONJ` (coordinate conjunction) and `SCONJ` (subordinate conjunction). `NONLEX` is splitted into `X` (foreign words, unknown words) and `SYM` (symbols). Besides that, punctuation marks are explicitly tagged `PUNCT` in UD.   
In the intermediate schema (UD-X), an extended list of parts of speech is used which includes `ANUM`, `PRAEDIC`, `PARENTH`.

The following section lists some known mismatches in the annotation practice of RNC and UD.

* _и_, _е_, _я_ are tagged `SPRO` (UD: `PRON`), the same way as in OldRus. 
* _иже_, _еже_, _яже_ are tagged `SPRO` in RNC and `PRON` in UD. (There is some incosistency in OldRus in this respect, but they are mostly tagged `APRO` there).  
* _который_, _кыиждо_, _кыиже_ are tagged `APRO` in RNC and `PRON` in UD. The reason is that it has the morphological properties of an adjective and the syntactic properties of a noun (nominal head).  
* the possessives _его_, _ея_, _ee_, _ихъ_, etc. are tagged as the Genitive forms of _онъ_, _оно_, _она_, _онѣ_: `PRON`, `Case=Gen`. (In OldRus, they are tagged as the Genitive forms of _и_; in ModernRus, they are tagged as indeclinable adjectival pronominals _его_, _ее_, _их_).  

* the list of `APRO` (UD: `DET`) includes:
  * interrogative, relative, negative adjectival pronouns, quantifiers: _каковый_, _никакий_, _вьсь_   
  * deictic (demonstrative) words: _сей_, _овъ_, _таковый_, etc.  
  * possessive adjectival pronouns: _мой_, _свой_, etc.  
  
* the numeral _один_ is tagged `ANUM` in RNC and `NUM` in UD. The reason to tag it `ANUM` is that it has an adjective-like paradigm and is used as an attribute (in Nominative case, it does not govern the Genitive case of the noun phrase as other numerals, see Zaliznjak 2003). However, the tag `NUM` is applied consitently to its lexical equivalents throughout the UD treebanks. In OldRus, the tag `NUM` is used as well.

* the predicative words (RNC: `PRAEDIC`) include the following categories:  
  * _-о_, _-е/ѣ_ forms that have corresponding adjectives: (_ночью_) _тяпло_, _пригоже_, _явно_, etc. -- tagged as the short neutral forms of adjectives: `ADJ`, `Gender=Neut`, `Number=Sing`, `Variant=Short` in UD.  
  * modal words: _можно_, _льзѣ_, _надобно_, _уне_ -- tagged as `VERB` in UD.  
  * _нѣтъ_, _нѣ_ -- tagged as `VERB` in UD.  
  * nouns such as _пора_ use predicatively (cf. _пора идти_) -- tagged as `S` in RNC and `NOUN` in UD.  
  * interjections, onomatopoeic words used predicatively  -- tagged as `INTJ`.   
  
* `AUX` is used to tag:
  * the auxiliary use of _быти_, _имѣти_, _хотѣти_ in the analytical grammatical forms  
  * the conditional markers _бы_, _б_ (originally, also the forms of _быти_) in the analytical grammatical forms  
  * the copula use of _быти_ in nominal clauses  
  * the reflexive markers (clitics) _си_, _ся_
Only the existential and locative uses of the verb _быти_ are tagged `VERB`.  
  
* Within the named entities:
  * patronymics are tagged `S` (UD: `PROPN`): _Васильевичю_  
  * last (family) names are tagged `S` (UD: `PROPN`): _Колюбакинымъ_.  
In OldRus, the patronymics are tagged as nouns while the last names are tagged as adjectives: `A`+`as_persn` (cf. _кнѧгиню Кондратовѹю_).  


### Grammatical features

#### Animacy  

Animacy (`anim`; UD: `Animacy=Anim`) is tagged in Accusative construction in which the form of Accusative is equal to the Genitive form): _брата нашег\[о\] молодшег\[о\]_. The opposite case, when the Accusative case form is equal to the Nominative form, is not tagged.


#### L-form (indeclinable perfective participle)  

_Л_-participles (cf. _взялъ_) are tagged `perf` (UD: `VerbForm=PartRes` + `Tense=Past`), to distinguish them from other participles (cf. взявъ: `past partcp`; UD: `VerbForm=Part` + `Tense=Past`). The tense tag in UD will allow one to map the MidRus l-forms to the ModernRus past forms. L-forms are used both on their own and within the analystical forms, see [below]().  


#### Gerundive (indeclinable adverbial participle)  

According to Zalizniak 2004, forms such as _уповая_, _слышев_ are considered indeclinable gerundives:  
* `ger` (UD: `VerbForm=Conv`).  


### Analytical forms  

The analytical forms are annotated as two (or more) tokens cross-linked at the morphological (cf. OldRus) and syntactic (UD) level. All tokens are tagged `analyt` (UD: `Analyt=Yes`), the grammatical features are labeled on the token in which they are expressed:  

(1)
\[RNC-MidRus\]
```
а       <ana lex="а" gr="CONJ"></ana>
будет   <ana lex="быти" gr="V,3p,act,analyt,fut,fut2,indic,intran,sg" gr_ext="IN:FUT2+3312"></ana>
не      <ana lex="не" gr="PART"></ana>
дошла   <ana lex="доити" gr="V,act,f,intran,perf,pf,sg" gr_ext="IN:FUT2+3310"></ana>
```

\[UD-MidRus\]
```
1 а       а     CCONJ _ _                                                                 4 cc
2 будет   быти	AUX 	_ Analyt=Yes|Mood=Ind|Number=Sing|Person=3|Tense=Fut,Fut2|Voice=Act   4 aux
3 не      не	PART    _ Polarity=Neg                                                    4 advmod
4 дошла   доити	VERB	_ Analyt=Yes|Aspect=Perf|Gender=Fem|Number=Sing|Tense=Past|
                        Transit=Tran|VerbForm=PartRes|Voice=Act                           0 root
```

In example (1), number and person are labeled on the auxiliary _будет_, and gender and number are labeled on the content verb _дошла_. The content verb is also tagged `perf` (UD: `Tense=Past`, `VerbForm=PartRes`) whereas the auxiliary is labeled by the tense of the token and the tense of the whole analytical form `fut2` (UD: `Tense=Fut2`). Furthermore, _будет_ is tagged `AUX` (part of speech) and `aux` (dependency relation) in UD. 

The list of the analytical forms includes:  

* analytical future (new form, attested starting from the 1600s): infinitive + the future form of _быти_ (_буду_, _будешь_), cf. _буду просить_
  - the auxiliary is tagged `analyt` + `fut` (UD: `Analyt=Yes` + `Tense=Fut`)  

* future 1: infinitive + the auxiliary nonpast forms of _хотѣти_, _имѣти_, _почати_, _начати_, _учати_, _стати_, cf. _имет обидѣти_
  - the auxiliary is tagged `analyt` + `fut1` (UD: `Analyt=Yes` + `Tense=Fut1`)  

* future 2: l-form + the future form of _быти_ (_буду_, _будешь_), cf. _гдѣ  бꙋдеш_[_ь_] _хотѧ послал_, _бѹдѹ задѣла_
  * or infinitive + the auxiliary future form of _яти_, cf. _имꙋ любѡв_[_ь_] _имати_  
    - the auxiliary is tagged `analyt` + `fut2` (UD: `Analyt=Yes` + `Tense=Fut2`)  

* analytical perfect: l-form and the 1st and 2nd person auxiliary in the present tense (_есмь_, _еси_, etc.), cf. _взѧл
еси_ 
  - the auxiliary is tagged `analyt` + `perf` (UD: `Analyt=Yes` + `Tense=Perf`)  

* pluperfect (plusquamperfect): l-form + the perfect form of _быти_, cf. ON _реклъ iеси былъ_, 
  - the auxiliary is tagged `analyt` + `pqperf` (UD: `Analyt=Yes` + `Tense=Pqp`)  

* subjunctive (conditional): l-form + _бы_, _б_ (the aorist form of _быти_) (or conjunctions that incorporate -_бы_: _чтоб_(_ы_), _абы_, etc.), cf. _я бы сталъ_, _чтоб онъ пожаловалъ_ 
  - the auxiliary (or conjunction) is tagged `cond` (UD: `Mood=Cnd`)  

* subjunctive 2 (conditional 2): l-form + _бы еси_, _бы есте_ (2nd person forms of быти), cf. _держали бы есте_ (_веру християнскую_)  
  - the auxiliary _бы_ is tagged `analyt` + `cond2` (UD: `Mood=Cnd2`), _еси_ is tagged `analyt` + `in\_cond`   
 
The optative construction _да_ + present is not considered the analytical form.  


### Optional tags

#### Features not available in automatic annotation 

The following tags of OldRus can be defined only in a particular context, often with the assistance of encyclopedic knowledge.  In RNC-MidRus, they can be used optionally in manual annotation.  
* `as_S` (substantivized)  -- tagged `AdjType=Subst` in UD.  
* `as_persn` (used as a personal name) -- tagged `AdjType=Subst` in UD.   
* `as_topn` (used as a toponym) -- tagged `NounType=Topon` in UD.   
* `as_ethn` (used as ethnonym) -- tagged `NounType=Ethn` in UD.    
* `as_ADV` (used as an adverb): _придоша Ветрѹ вечеръ_ (UD: `NOUN`+`NounType=Adv`), _по готовѹ_ (UD: `ADJ`+`AdjType=Adv`)  
* `as_PART` (used as a particle): _хотя_ (UD: `NOUN`+`NounType=Adv`), _по готовѹ_ (UD: `ADJ`+`AdjType=Adv`)  
* `as_PARENTH` -- tagged `PARENTH` in RNC-MidRus (UD: `ADV`+`AdvType=Parenth`).  
* `as_PRAEDIC` -- tagged `PRAEDIC` in RNC-MidRus (UD: `ADJ`+`AdjType=Praedic`).  
* `as_deb` (used as debitive): _да не съгрѣшѫ тебѣ_ (UD: `VERB`+`VerbType=Debit`))  
* `as_CONJ` (used as a conjunction) -- not tagged in RNC-MidRus, labeled with `cc` or `mark` dependency relation in UD.  
* `as_voc` (vocative use) -- not tagged in RNC-MidRus, labeled with `vocative` dependency relation in UD.  
* `as_PRO` (used as pronoun)  -- not tagged in RNC-MidRus and UD.   
* `as_ART` (used as article) -- not applicable in RNC-MidRus

The following tags can be used optionally and only in the RNC-style annotation.  
* `in_persn`: (_анастасу_) _корсунѧнину_  
* `in_ethn`: _чернии клобѹци_  
* `in_topn`: _костѧни градѣ_  
* `in_ADV`: _тако же_  
* `in_NUM`: _ѡдиныи на десѧте_, _.҂ѕ҃. ѱ҃. аӏ҃._  
* `in_CONJ`: _єгда како_  
* `in_PR`: _в мѣсто_  

* `husbn`: (_ѹ_) _тѹдоровѣи_, distinguishes the name given by husband's name from patronymics in the Birchbark Letters corpus.  

Old nicknames are not considered last names and are tagged `as_persn` (UD: `NounType=Persn`): _Мономахъ_.


#### Spelling and grammatical variants

* `distort` (UD: `Typo=Yes`) -- used to tag distorted words and guessed words. In addition, there is a tag [`Echo`](https://universaldependencies.org/u/feat/Echo.html) in UD used for various repetitions.
* `anom` (not tagged in UD) -- used to tag grammatically anomalous forms. However, what is considered 'grammatically anomalous' in the historical data is controversial and theory-specific. So, this tag should be used with caution.   
* `oov` (cf. `bastard` in ModernRus, not tagged in UD) -- used to tag words not seen in the training data or the grammatical dictionary of the tagger.  
* `abbr` (UD: `Abbr=Yes`) -- used to tag abbreviated words including those marked by titlo (◌҃).  
* `ciph` (UD: `NumForm=Digit`) -- used to tag cardinal and ordinal numerals expressed by (Euro-Arabic) digits and Cyrillic letters   


### Extended annotation schema 

We introduce the notion of extended features (or x-features) that are added into annotation to meet the needs of micro-diachronic studies in which the data of the modern language are compared against the historical data. Even if a certain grammatical category is under development and it is not evident if it is present or absent in the data, x-features allows one to look for the potentially interesting patterns. In the current Middle Russian standard, the x-features include:  

* `anim$` and `inan$` (UD: `Animacy[lex]=Anim`, `Animacy[lex]=Inan`): classifying features that correspond to `anim` and `inan` in the ModernRus annotation. This category is not to be mixed with `anim` (UD: `Animacy=Anim`) that is applicable only to the Accusative constructions (see [above]()). There are cases in which the lexically animated nouns (`anim$`) are not tagged as `anim`.  

* In UD-MidRus, `persn`, `patrn`, `famn`, `zoon`, `ethn`, `topon` are considered extended features and tagged under the category `NounType` (e.g. `NounType=Ethn`).  


### Simplified annotation schema  

In order to make inventories of UD Church Slavic (UD-PROIEL) and UD-MidRus compatible, the following features can be excluded from annotation:
* `Aspect`    
* `Transit` (transitivity)  
* `Reflex` (reflexive)   
* `Animacy` (Acc=Gen)  
* `Variant` (long/short forms)  
* `Strength` (in PROIEL)
* `PronType` (in PROIEL)

Except for Variant/Strength and Animacy, these features are lexical (classifying) and do not add to the identification of which paradigm cell the form fills. 
Obviously, extended and optional features are out of the simplified list as well.  

The tense forms of aorist (`Tense=Aor`) and imperfect (`Tense=Imp`) is relabeled as `Tense=Past` (the same way as in UD-PROIEL/TOROT).  


