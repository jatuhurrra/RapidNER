# rapidner (still  under development)

[![arXiv](https://img.shields.io/badge/6029236-B31B1B.svg)](https://arxiv.org/abs/6029236)

<h3>Overview</h3>
Rapid development of new NER datasets needed to train and fine-tune language models under new domains is an expensive endeavor. To ensure faster development of NER datasets, we introduce *RapidNER*, a new annotation method. RapidNER is scalable and flexible to any domain. We focused on *human-robot interaction (HRI)* and developed a dataset whose named entities are relevant to train a robot in the HRI domain.

<h3>The Dataset</h3>
We leverage the RapidNER framework to create **NERsocial**, a new dataset containing 153K tokens, 134K entities, and 99.4K sentences across six entity types: **drinks, foods, hobbies, jobs, pets, sports**

***

```
{ 
'tokens': {"0": ["Poco", "Bueno", "was", "a", "American", "Quarter", "Horse", "stallion", "foaled", "April", "10", ",", "1944", "."], "1": ["Formal", "breeds", "often", "considered", "to", "be", "of", "the", "pit", "bull", "type", "include", "the", "American", "Pit", "Bull", "Terrier", ",", "American", "Staffordshire", "Terrier", ",", "American", "Bully", ",", "and", "Staffordshire", "Bull", "Terrier", "."], ... },
 'tags': {"0": ["O", "O", "O", "O", "B-PET", "I-PET", "I-PET", "O", "O", "O", "O", "O", "O", "O"], "1": ["O", "O", "O", "O", "O", "O", "O", "O", "B-PET", "I-PET", "O", "O", "O", "O", "B-PET", "I-PET", "I-PET", "O", "B-PET", "I-PET", "I-PET", "O", "B-PET", "I-PET", "O", "O", "B-PET", "I-PET", "I-PET", "O"], ...}
 }
```
***
The two dictionaries `label2id` and `id2label` are shown below: 

Dictionary One: `label2id`
```
{'B-JOB': 0,
 'B-PET': 1,
 'I-PEOPLENAME': 2,
 'B-PEOPLENAME': 3,
 'I-COUNTRY': 4,
 'O': 5,
 'I-ORG': 6,
 'I-JOB': 7,
 'B-COUNTRY': 8,
 'I-PET': 9,
 'B-ORG': 10}
```
Dictionary Two: `id2label`
```
{0: 'B-JOB',
 1: 'B-PET',
 2: 'I-PEOPLENAME',
 3: 'B-PEOPLENAME',
 4: 'I-COUNTRY',
 5: 'O',
 6: 'I-ORG',
 7: 'I-JOB',
 8: 'B-COUNTRY',
 9: 'I-PET',
 10: 'B-ORG'}
 ```
 ***

Moreover, the RE dataset is of the format below:
```
{ 
'tokens': {"0": ["Poco", "Bueno", "was", "a", "American", "Quarter", "Horse", "stallion", "foaled", "April", "10", ",", "1944", "."], "1": ["Formal", "breeds", "often", "considered", "to", "be", "of", "the", "pit", "bull", "type", "include", "the", "American", "Pit", "Bull", "Terrier", ",", "American", "Staffordshire", "Terrier", ",", "American", "Bully", ",", "and", "Staffordshire", "Bull", "Terrier", "."], ... },
 'tags': {"0": ["O", "O", "O", "O", "B-PET", "I-PET", "I-PET", "O", "O", "O", "O", "O", "O", "O"], "1": ["O", "O", "O", "O", "O", "O", "O", "O", "B-PET", "I-PET", "O", "O", "O", "O", "B-PET", "I-PET", "I-PET", "O", "B-PET", "I-PET", "I-PET", "O", "B-PET", "I-PET", "O", "O", "B-PET", "I-PET", "I-PET", "O"], ...}
 }
```

<h3>Experiments</h3>
We deploy several LLMs for the NER and RE evaluation.

### Citation

If you find this work or dataset helpful in your research, please cite it as follows:

```

```
