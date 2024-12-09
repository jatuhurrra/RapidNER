# rapidner (still  under development)

[![arXiv](https://img.shields.io/badge/6029236-B31B1B.svg)](arXiv paper soon)
***

### :telescope: :telescope: Overview
Rapid development of new NER datasets needed to train and fine-tune language models under new domains is an expensive endeavor. 
To ensure faster development of NER datasets, we introduce *RapidNER*, a new annotation method. 
RapidNER is scalable and flexible to any domain. RapidNER relies on *Elasticsearch* and the *Wikidata* knowledge graph to create a new NER dataset. 
We focused on *human-robot interaction (HRI)* and developed a dataset whose named entities are relevant to train a robot in the HRI domain. 

<p align="center">
  <img src="/images/Intro_dataset_process2.png" width="85%" alt="Results">
</p>

### 🤖 🤖  Human-Robot Interaction (HRI)
We envision a scenario in which the human and the robot engage in discussion over a wide range of topics, in *daily conversation* settings, such as in a cafe, restaurant, social events, etc. We introduced six entity types or named entities (NEs) to begin with, and additional NEs wold be added later.

### :mag: :mag: Elasticsearch 
We collected thousands of sentences from Wikipedia and used Elasticsearch to select and return only the sentences that contained *mentions* of the six NEs introduced above. 
In addition, we used Elasticsearch to mark the spans of text inside the sentence that correspond to the *entity mentions* in that sentence. 
In this way, we managed to expedite the annotation process for the NER dataset. 

###  :file_folder: :file_cabinet: The Dataset
We leverage the RapidNER framework to create **NERsocial**, a new dataset containing 153K tokens, 134K entities, and 99.4K sentences across six entity types: **drinks, foods, hobbies, jobs, pets, sports**

***

```
{ 
'tokens': {"0": ["Poco", "Bueno", "was", "a", "American", "Quarter", "Horse", "stallion", "foaled", "April", "10", ",", "1944", "."], "1": ["Formal", "breeds", "often", "considered", "to", "be", "of", "the", "pit", "bull", "type", "include", "the", "American", "Pit", "Bull", "Terrier", ",", "American", "Staffordshire", "Terrier", ",", "American", "Bully", ",", "and", "Staffordshire", "Bull", "Terrier", "."], ... },
 'tags': {"0": ["O", "O", "O", "O", "B-PET", "I-PET", "I-PET", "O", "O", "O", "O", "O", "O", "O"], "1": ["O", "O", "O", "O", "O", "O", "O", "O", "B-PET", "I-PET", "O", "O", "O", "O", "B-PET", "I-PET", "I-PET", "O", "B-PET", "I-PET", "I-PET", "O", "B-PET", "I-PET", "O", "O", "B-PET", "I-PET", "I-PET", "O"], ...}
 }
```

The two dictionaries `label2id` and `id2label` are shown below: 

Dictionary One: `label2id`
```
labels_to_ids = {
    'B-DRINK': 0,
    'B-FOOD': 1,
    'B-HOBBY': 2,
    'B-JOB': 3,
    'B-SPORT': 4,
    'I-DRINK': 5,
    'I-FOOD': 6,
    'I-HOBBY': 7,
    'I-JOB': 8,
    'I-SPORT': 9,
    'O': 10
}
```
Dictionary Two: `id2label`
```
ids_to_labels = {v: k for k, v in labels_to_ids.items()}
 ```

### :gear: :wrench: Experiments
We deploy several LLMs for the NER and RE evaluation.

### :bookmark_tabs: :scroll: Citation

If you find this work or dataset helpful in your research, please cite it as follows:

```
Citation coming soon
```
