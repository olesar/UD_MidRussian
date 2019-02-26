### A Middle Russian tagset for UD 2.0

Created: 17 Feb 2019

## Parts of speech (UPOS)

|UPOS tag|Description (ru)|Description (en)|Freq|Examples|RNC|
|---|---|---|---|---|---|
|ADJ|прилагательное,порядковое числительное|adjective| | |A,ANUM|
|ADP|предлог|preposition| | |PR|
|ADV|наречие, местоимение-наречие|adverb| | |ADV,ADVPRO,PARENTH|
|AUX|вспомогательный грамматический показатель|auxiliary| | |(V)|
|CCONJ|сочинительный союз|coordinating conjunction| | |CONJ|
|DET|местоимение-прилагательное|determiner (adjectival pronoun)| | |APRO|
|NOUN|существительное (нарицательное)|noun| | |S|
|NUM|числительное|numeral| | |NUM|
|PART|частица|particle| | |PART|
|PRON|местоимение-существительное|pronoun (nominal)| | |SPRO|
|PROPN|существительное (собственное)|proper noun| | |(S)|
|PUNCT|пунктуация|punctuation mark| | |--|
|SCONJ|подчинительный союз|subordinating conjunction| | |CONJ|
|SYM|символ|symbol| | |(X)|
|VERB|глагол (вкл. причастие, деепричастие)|verb| | |V|
|X|другое|foreign and non-words| | |NONLEX|


## Grammatical features (FEAT)

Status: 
- \_* the category/value occurs in a part of the word paradigm,  
- ** the category/value applies to a particular lexical class  
- *** not included in UD 2.0 standard


|Cat|Feat|Status|Description (ru)|Description (en)|Freq|Examples|RNC|
|---|---|---|---|---|---|---|---|
|ADJ| Animacy=Anim | * | одушевленность | animate (Acc=Gen) | | | acc |
|ADJ| Animacy=Inan | * | неодушевленность | inanimate (Acc=Nom) | | | dat |
|ADJ| Case=Acc | * | падеж: винительный | case: accusative | | | acc |
|ADJ| Case=Dat | * | падеж: дательный | case: dative | | | dat |
|ADJ| Case=Gen | * | падеж: родительный | case: genitive | | | gen |
|ADJ| Case=Ins | * | падеж: творительный | case: instrumental | | | ins |
|ADJ| Case=Loc | * | падеж: предложный | case: locative| | | loc |
|ADJ| Case=Nom | * | падеж: именительный | case: nominative | | | nom |
|ADJ| Degree=Cmp | ** | степень: сравнительная | degree: comparative | | | comp |
|ADJ| Degree=Cmp2 | ** | степень: 2-я сравнительная | degree: comparative | | | comp2 |
|ADJ| Degree=Pos | ** | степень: положительная | degree: positive | | | -- |
|ADJ| Gender=Fem | * | род: женский | gender: feminine | | | f |
|ADJ| Gender=Masc | * | род: мужской | gender: masculine | | | m |
|ADJ| Gender=Neut | * | род: средний | gender: neutral | | | n |
|ADJ| Number=Dual | * | число: двойственное | number: dual | | | du |
|ADJ| Number=Plur | * | число: множественное | number: plural | | | pl |
|ADJ| Number=Sing | * | число: единственное | number: singular | | | sg |
|ADJ| Variant=Long | ** | полное окончание | long ending | | | plen |
|ADJ| Variant=Short | ** | краткое окончание | short ending | | | brev |
|ADJ| _ | ** | нет помет | no tags | |ѳ҃.и | -- |

Tag combinations:
* Case Degree Gender Number Variant -- default  
  * Case Degree Number Variant -- + plural (dual, if any) oblique, long forms  
  * Animacy Case Degree Gender Number Variant -- + Accusative in which Acc=Gen  
    * Animacy Case Degree Number Variant -- + plural Accusative  
* Degree -- indeclinable comparative form  
* Case Degree Gender Number -- possessives?, oblique forms w/o long/short constrast?  
  * Case Degree Number -- + plural oblique  
  * Animacy Case Degree Gender Number -- + Accusative in which Acc=Gen  
     * Animacy Case Degree Number -- + plural Accusative   
* Case Gender Number Variant -- ordinal numerals  
  * Case Number Variant -- + plural oblique  
  * Animacy Case Gender Number -- + Accusative in which Acc=Gen  
     * Animacy Case Number -- + plural Accusative   
* Degree Gender Number Variant -- short predicative adjectives  
  * Degree Number Variant -- + plural oblique  
* _ -- digit-based ordinal numerals, indeclinable adjectives  

NB Degree=Comp is also labeled on lexical comparatives such as _лутшии_. 


|Cat|Feat|Status|Description (ru)|Description (en)|Freq|Examples|RNC|
|---|---|---|---|---|---|---|---|
|ADV| Degree=Cmp | ** | степень: сравнительная | degree: comparative | | | comp |
|ADV| Degree=Cmp2 | ** | степень: 2-я сравнительная | degree: comparative | | | comp2 |
|ADV| Degree=Pos | ** | степень: положительная | degree: positive | | | (posit) |
|ADV| _ | ** | -- | (pronominal adverbs) | | | -- |

Tag combinations:
* Degree -- default  
* _ -- pronominal adverbs 


|Cat|Feat|Status|Description (ru)|Description (en)|Freq|Examples|RNC|
|---|---|---|---|---|---|---|---|
|DET| Animacy=Anim | * | одушевленность | animate (Acc=Gen) | | | acc |
|DET| Animacy=Inan | * | неодушевленность | inanimate (Acc=Nom) | | | dat |
|DET| Case=Acc | * | падеж: винительный | case: accusative | | | acc |
|DET| Case=Dat | * | падеж: дательный | case: dative | | | dat |
|DET| Case=Gen | * | падеж: родительный | case: genitive | | | gen |
|DET| Case=Ins | * | падеж: творительный | case: instrumental | | | ins |
|DET| Case=Loc | * | падеж: предложный | case: locative| | | loc |
|DET| Case=Nom | * | падеж: именительный | case: nominative | | | nom |
|DET| Gender=Fem | * | род: женский | gender: feminine | | | f |
|DET| Gender=Masc | * | род: мужской | gender: masculine | | | m |
|DET| Gender=Neut | * | род: средний | gender: neutral | | | n |
|DET| Number=Dual | * | число: двойственное | number: dual | | | du |
|DET| Number=Plur | * | число: множественное | number: plural | | | pl |
|DET| Number=Sing | * | число: единственное | number: singular | | | sg |
|DET| Poss=Yes | ** | посессивное | possessive | | _свой_, _мой_ | poss |
|DET| Variant=Long | ** | полное окончание | long ending | | | plen |
|DET| Variant=Short | ** | краткое окончание | short ending | | | brev |

Tag combinations:
* Case Gender Number -- default (_сам_)  
  * Case Number -- + plural oblique (_всѣми_)  
  * Animacy Case Gender Number -- + Accusative in which Acc=Gen (_которого_)  
     * Animacy Case Number -- + plural Accusative (_всѣх_)   
* Case Gender Number Poss -- possessive (_мой_)  
  * Case Number Poss -- + plural oblique (_своими_)  
  * Animacy Case Gender Number Poss -- + Accusative in which Acc=Gen (_своего_)  
     * Animacy Case Number Poss -- + plural Accusative (_своих_)   
* Case Gender Number Variant -- determiners with contrast between long and short forms?  
  * Case Number Variant -- + plural oblique  
  * Animacy Case Gender Number -- + Accusative in which Acc=Gen  
     * Animacy Case Number -- + plural Accusative  
     

|Cat|Feat|Status|Description (ru)|Description (en)|Freq|Examples|RNC|
|---|---|---|---|---|---|---|---|
|NOUN| Animacy=Anim | * | одушевленность | animate (Acc=Gen) | | | acc |
|NOUN| Animacy=Inan | * | неодушевленность | inanimate (Acc=Nom) | | | dat |
|NOUN| Case=Acc | | падеж: винительный | case: accusative | | | acc |
|NOUN| Case=Dat | | падеж: дательный | case: dative | | | dat |
|NOUN| Case=Gen | | падеж: родительный | case: genitive | | | gen |
|NOUN| Case=Ins | | падеж: творительный | case: instrumental | | | ins |
|NOUN| Case=Loc | | падеж: предложный | case: locative| | | loc |
|NOUN| Case=Nom | | падеж: именительный | case: nominative | | | nom |
|NOUN| Case=Voc | | падеж: звательный | case: vocative | | | voc |
|NOUN| Gender=Fem | | род: женский | gender: feminine | | | f |
|NOUN| Gender=Masc | | род: мужской | gender: masculine | | | m |
|NOUN| Gender=Neut | | род: средний | gender: neutral | | | n |
|NOUN| Number=Dual | | число: двойственное | number: dual | | | du |
|NOUN| Number=Plur | | число: множественное | number: plural | | | pl |
|NOUN| Number=Sing | | число: единственное | number: singular | | | sg |

Tag combinations:
* Case Gender Number -- default  
  * Animacy Case Gender Number -- + Accusative in which Acc=Gen  
* Case Number -- rare cases in which one cannot label gender in the pluralia tantum nouns 
 

|Cat|Feat|Status|Description (ru)|Description (en)|Freq|Examples|RNC|
|---|---|---|---|---|---|---|---|
|NUM| Case=Acc | | падеж: винительный | case: accusative | | | acc |
|NUM| Case=Dat | | падеж: дательный | case: dative | | | dat |
|NUM| Case=Gen | | падеж: родительный | case: genitive | | | gen |
|NUM| Case=Ins | | падеж: творительный | case: instrumental | | | ins |
|NUM| Case=Loc | | падеж: предложный | case: locative| | | loc |
|NUM| Case=Nom | | падеж: именительный | case: nominative | | | nom |
|NUM| Gender=Fem | ** | род: женский | gender: feminine | | | f |
|NUM| Gender=Masc | ** | род: мужской | gender: masculine | | | m |
|NUM| Gender=Neut | ** | род: средний | gender: neutral | | | n |
|ADJ| _ | ** | нет помет | no tags | | _и_ | -- |

Tag combinations:
* Case -- default  
* Case Gender -- small numbers (_дву_, _обѣ_)  
* _ -- digit-based numerals  
NB _два_ can be labeled with Number=Dual (cf. _въ дву посаду_).
NB in UD standard, одинъ is cosidered a numeral and is labeled with Number. In RNC standard, it is considered ANUM (i.e. ADJ).


|Cat|Feat|Status|Description (ru)|Description (en)|Freq|Examples|RNC|
|---|---|---|---|---|---|---|---|
|PART| Polarity=Neg | ** | отрицательное | negative polarity | | _не_, _нѣ_, _ни_ | -- |
|PART| _ |  | нет помет | no tags | | _да_ | -- |


|Cat|Feat|Status|Description (ru)|Description (en)|Freq|Examples|RNC|
|---|---|---|---|---|---|---|---|
|PRON| Case=Acc | | падеж: винительный | case: accusative | | | acc |
|PRON| Case=Dat | | падеж: дательный | case: dative | | | dat |
|PRON| Case=Gen | | падеж: родительный | case: genitive | | | gen |
|PRON| Case=Ins | | падеж: творительный | case: instrumental | | | ins |
|PRON| Case=Loc | | падеж: предложный | case: locative| | | loc |
|PRON| Case=Nom | | падеж: именительный | case: nominative | | | nom |
|PRON| Gender=Fem | * | род: женский | gender: feminine | | | f |
|PRON| Gender=Masc | * | род: мужской | gender: masculine | | | m |
|PRON| Gender=Neut | * | род: средний | gender: neutral | | | n |
|PRON| Number=Dual | * | число: двойственное | number: dual | | | du |
|PRON| Number=Plur | * | число: множественное | number: plural | | | pl |
|PRON| Number=Sing | * | число: единственное | number: singular | | | sg |
|PRON| Person=1 | * | лицо: 1-е | person: 1st | | | 1p |
|PRON| Person=2 | * | лицо: 2-е | person: 2nd | | | 2p |
|PRON| Person=3 | * | лицо: 3-е | person: 3rd | | | 3p |
|PRON| Reflex=Yes | * | возвратное | reflexive | | | 3p |
|PRON| _ | ** | нет помет | indeclinable | | | -- |

Tag combinations:
* Case Number Person -- personal pronouns  
* Case Gender Number Person -- 3rd person pronouns  
* Case -- _кто_, _что_, _кождо_  
* Case Gender Number -- _се_, _всем_  
* Case Number -- _все_ (plural)
* Case Reflex -- _себѣ_ 


|Cat|Feat|Status|Description (ru)|Description (en)|Freq|Examples|RNC|
|---|---|---|---|---|---|---|---|
|PROPN| Animacy=Anim | * | одушевленность | animate (Acc=Gen) | | | acc |
|PROPN| Animacy=Inan | * | неодушевленность | inanimate (Acc=Nom) | | | dat |
|PROPN| Case=Acc | | падеж: винительный | case: accusative | | | acc |
|PROPN| Case=Dat | | падеж: дательный | case: dative | | | dat |
|PROPN| Case=Gen | | падеж: родительный | case: genitive | | | gen |
|PROPN| Case=Ins | | падеж: творительный | case: instrumental | | | ins |
|PROPN| Case=Loc | | падеж: предложный | case: locative| | | loc |
|PROPN| Case=Nom | | падеж: именительный | case: nominative | | | nom |
|PROPN| Case=Voc | | падеж: звательный | case: vocative | | | voc |
|PROPN| Gender=Fem | * | род: женский | gender: feminine | | | f |
|PROPN| Gender=Masc | * | род: мужской | gender: masculine | | | m |
|PROPN| Gender=Neut | * | род: средний | gender: neutral | | | n |
|PROPN| Number=Dual | * | число: двойственное | number: dual | | | sg |
|PROPN| Number=Plur | * | число: множественное | number: plural | | | pl |
|PROPN| Number=Sing | * | число: единственное | number: singular | | | du |

Tag combinations:
* Case Gender Number -- default  
  * Animacy Case Gender Number -- + Accusative in which Acc=Gen  


|Cat|Feat|Status|Description (ru)|Description (en)|Freq|Examples|RNC|
|---|---|---|---|---|---|---|---|
|SCONJ| Mood=Cnd | | наклонение: сослагательное | mood: conditional | | _чтобы_, _абы_ | cond |
|SCONJ| _ | | нет помет | indeclinable | | | -- |

|Cat|Feat|Status|Description (ru)|Description (en)|Freq|Examples|RNC|
|---|---|---|---|---|---|---|---|
|VERB| Aspect=Imp | ** | вид: несовершенный | aspect: imperfective | | | ipf |
|VERB| Aspect=Perf | ** | вид: совершенный | aspect: perfective | | | pf |
|VERB| Case=Acc | * | падеж: винительный | case: accusative | | | acc |
|VERB| Case=Dat | * | падеж: дательный | case: dative | | | dat |
|VERB| Case=Gen | * | падеж: родительный | case: genitive | | | gen |
|VERB| Case=Ins | * | падеж: творительный | case: instrumental | | | ins |
|VERB| Case=Loc | * | падеж: предложный | case: locative| | | loc |
|VERB| Case=Nom | * | падеж: именительный | case: nominative | | | nom |
|VERB| Gender=Fem | * | род: женский | gender: feminine | | | f |
|VERB| Gender=Masc | * | род: мужской | gender: masculine | | | m |
|VERB| Gender=Neut | * | род: средний | gender: neutral | | | n |
|AUX| Mood=Cnd | * | наклонение: сослагательное | mood: conditional | | _бы_, _б_ | cond |
|AUX| Mood=Cnd2 | * | наклонение: сослагательное 2 | mood: conditional | | _бы_, _б_ | cond2 |
|VERB| Mood=Imp | * | наклонение: повелительное | mood: imperative | | | imper |
|VERB| Mood=Ind | * | наклонение: индикатив | mood: indicative | | | indic |
|VERB| Number=Dual | * | число: двойственное | number: dual | | | 1p |
|VERB| Number=Plur | * | число: множественное | number: plural | | | 2p |
|VERB| Number=Sing | * | число: единственное | number: singular | | | 3p |
|VERB| Person=1 | * | лицо: 1-е | person: 1st | | | 1p |
|VERB| Person=2 | * | лицо: 2-е | person: 2nd | | | 2p |
|VERB| Person=3 | * | лицо: 3-е | person: 3rd | | | 3p |
|VERB| Tense=Aor | * | время: будущее | tense: aorist | | | aor |
|VERB| Tense=Fut | * | время: будущее | tense: future | | | fut |
|AUX| Tense=Fut1 | * | время: будущее 1 | tense: future 1st | | | fut1 |
|AUX| Tense=Fut2 | * | время: будущее 2 | tense: future 2nd | | | fut2 |
|VERB| Tense=Imp | * | время: имперфект | tense: imperfect | | | iperf, imperf |
|VERB| Tense=Past | * | время: прошедшее | tense: past | | | praet,past |
|AUX| Tense=Pqp | * | время: плюсквамперфект | tense: pluperfect | | | pqperf |
|VERB| Tense=Pres | * | время: настоящее | tense: present | | | praes |
|VERB| Variant=Long | * | полное окончание | long ending | | | plen |
|VERB| Variant=Short | * | краткое окончание | short ending | | | brev |
|VERB| VerbForm=Conv | | деепричастие | converb, gerundive | | | ger |
|VERB| VerbForm=Fin | | финитный | finite | | | (fin) |
|VERB| VerbForm=Inf | | инфинитив | infinitive | | | inf |
|VERB| VerbForm=Part | | причастие | participle | | | partcp |
|VERB| VerbForm=PartRes | | л-форма | l-form | | | perf |
|VERB| VerbForm=Sup | | супин | supine | | | sup |
|VERB| Voice=Act | * | залог: активный | voice: active | | | act |
|VERB| Voice=Mid | | залог: средний | voice: middle (reflexive verbs) | | | med |
|VERB| Voice=Pass |  | залог: пассивный | voice: passive | | | pass |
|VERB| _ | ** | нет помет | indeclinable _нѣтъ_ | | | -- | 
|AUX| _ | ** | нет помет | indeclinable _си_, _ся_ | | | -- | 

Tag combinations:
* Aspect VerbForm Voice -- infinitive  
* Aspect Tense VerbForm Voice -- converb  
* Aspect Mood Number Person Tense VerbForm Voice -- personal forms in indicative  
* Aspect Gender Mood Number Tense VerbForm Voice -- l-forms (labeled as Tense=Past, VerbForm=PartRes)   
* Aspect Case Gender Number Strength Tense VerbForm Voice - participles  
  * Aspect Case Number Strength Tense VerbForm Voice - plural participles  
* _ -- _нѣтъ_ (indeclinable)

NB Transitivity is marked in the RNC standard: Transit=Tran, Transit=Intr

AUX - see VERB

### Indeclinable: 

|Cat|Feat|Status|Description (ru)|Description (en)|Freq|Examples|RNC|
|---|---|---|---|---|---|---|---|
|ADP| _ | | нет помет | indeclinable | | | -- |
|CCONJ| _ | | нет помет | indeclinable | | | -- |
|INTJ| _ | | нет помет | indeclinable | | | -- |
|PART| _ | | нет помет | indeclinable | | | -- |
|PUNCT| _ | | нет помет | indeclinable | | | -- |
|SYM| _ | | нет помет | indeclinable | | | -- |
|X| _ | | нет помет | indeclinable | | | -- |


### Additional features
* Abbr=Yes  
* Analyt=Yes  
* ...Type=
* Other=


### Notes on the annotation in other schemas

TOROT has the following features:
* Strength=Weak, Strength=Strong (corresponds to Variant=Long, Variant=Short)  
* PronType -- in pronominals  
* Poss -- in adjectival pronominals (ADJ)  
* Reflex -- in adjectival pronoun _свой_ (ADJ)  
* Aspect=Res -- for l-forms (labeled VerbForm=Part, no Tense)  
Aspect, Transit, Animacy not tagged.

* _не_, _ни_, _нѣ_ -- labeled ADV  
* _сеѭ_, _моею_, _своею_, вь҆сѣмъ_ -- labeled ADJ
* _она_ etc. -- labeled ADJ
