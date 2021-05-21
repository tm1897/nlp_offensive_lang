# Natural Language Processing - Offensive language exploratory analysis. 
Offensive speech is often present on the Internet. Many times this is not desirable on the pages, or it is forbidden, so we want to detect it automatically. This task has attracted a lot of attention recently, and as a result, many language processing techniques and algorithms have been developed. In this report, we present the capabilities of a number of traditional and state-of-the-art methods. Furthermore, we try to produce meaningful visualizations of the peculiarities of the different types of hate speech, as well as construct an offensive language schema based on the drawn conclusions from the analyses.

## Running the notebooks

To run any notebook from this repository, you first have to create a conda environment from the [nlp_project_env.yml](nlp_project_env.yml)
 file. Most of the data required by notebooks are already in this repository. If not, there are instructions on where to get it, and how to set it up inside the notebook. 
 For preprocessing the data, we prepared [CombiningDataset.ipynb](CombiningDataset.ipynb) notebook. 
 Other notebooks are used for exploring the data and running the models. Pre-trained models need to be downloaded from [here](https://drive.google.com/drive/folders/1aVx98DSCBQp-yYR3kfggDmXiIGFrX7aX?usp=sharing "Pre-trained models"), and in the notebook set the correct path to the downloaded model.


The BERT embeddings notebook is available as a [Google Colab notebook](https://colab.research.google.com/drive/1B2cXLxr0KNy6RLQcntvaRkfAmkICVF2L?usp=sharing).


## Data
### A Benchmark Dataset for Learning to Intervene in Online Hate Speech
[data directory](data/reddit_binary-jing-qian)

- English
- Reddit
- 22,324
- Binary (hateful/not)
- https://arxiv.org/pdf/1909.04251.pdf
- https://github.com/jing-qian/A-Benchmark-Dataset-for-Learning-to-Intervene-in-Online-Hate-Speech

### Automated Hate Speech Detection and the Problem of Offensive Language
[data directory](data/twitter_hierarchy_t-davidson)

- English
- Twitter
- 24,802
- Hierarchy (Hate, Offensive, Neither)
- https://arxiv.org/abs/1703.04009
- https://github.com/t-davidson/hate-speech-and-offensive-language

### Hate Speech Dataset from a White Supremacy Forum
[data directory](data/stormfront_ternary_vicomtech)

- English
- Stormfront (Forum)
- 9,916
- Ternary (Hate, Relation, Not)
- https://www.aclweb.org/anthology/W18-5102/
- https://github.com/Vicomtech/hate-speech-dataset


### Large Scale Crowdsourcing and Characterizatio n of Twitter Abusive Behavior
[data directory](data/twitter_large_scale_crownsourcing_founta)

- English
- Twitter
- 80,000
- Multi-thematic (Abusive, Hateful, Normal, Spam)
- https://arxiv.org/pdf/1802.00393.pdf 
- https://dataverse.mpi-sws.org/dataset.xhtml?persistentId=doi:10.5072/FK2/ZDTEMN 

- Just ID's of tweets. 

### A Large Labeled Corpus for Online Harassment Research

- English
- Twitter
- 35,000
- Binary (Harassment, Not)
- https://www.cs.umd.edu/~golbeck/papers/trolling.pdf

- Write to jgolbeck@umd.edu to get data (agree to a Data Terms of Use which includes ethical considerations.)


### Ex Machina: Personal Attacks Seen at Scale, Personal attacks

- Detecting Insults in Social Com-mentary


- English
- Wikipedia posts
- Binary (Personal attack, Not)
- https://arxiv.org/pdf/1610.08914.pdf
- https://github.com/ewulczyn/wiki-detox


### Ex Machina: Personal Attacks Seen at Scale, Toxicity

- English
- Wikipedia posts
- Binary (Personal attack, Not)
- https://arxiv.org/pdf/1610.08914.pdf
- https://github.com/ewulczyn/wiki-detox


## Detecting cyberbullying in online communities
[data directory](data/wow)

- English
- World of Warcraft, posts
- 16,975
- Binary (Harassment, Not)
- https://aisel.aisnet.org/cgi/viewcontent.cgi?article=1061&context=ecis2016_rp
- http://ub-web.de/research/
- SQL dataset

## Detecting cyberbullying in online communities
[data directory](data/lol)

- English
- League of Legends, posts
- 16,975
- Binary (Harassment, Not)
- https://aisel.aisnet.org/cgi/viewcontent.cgi?article=1061&context=ecis2016_rp
- http://ub-web.de/research/
- SQL dataset


## A Quality Type-aware Annotated Corpus and Lexicon for Harassment Research

- English
- Twitter
- 24,189
- Multi-topic harassment detection
- https://arxiv.org/pdf/1802.09416.pdf
- https://github.com/Mrezvan94/Harassment-Corpus (just a harassment lexicon)

## Ex Machina: Personal Attacks Seen at Scale, Aggression and Friendliness

- English
- Wikipedia
- 160,000
- Aggression/friendliness
- https://github.com/ewulczyn/wiki-detox (dataset needs to be generated)

### Hateful Symbols or Hateful People? Predictive Features for Hate speech Detection on Twitter
[data directory](data/hateful_symbols_or_hateful_people_predictive_features_for_hate_speech_detection_on_twitter)

- English
- Twitter
- 16,914
- Ternary (Racist, Sexist, Neither)
- paper: https://www.aclweb.org/anthology/S19-2.pdf
- github: https://github.com/zeerakw/hatespeech
- only Twitter IDs

### Detecting Online Hate Speech Using Context Aware Models
[data directory](data/detecting_online_hate_speech_using_context_aware_models)

- English
- FoxNews, posts
- 1,528
- Binary (Hate, Not)
- paper: https://arxiv.org/pdf/1710.07395.pdf
- github: https://github.com/sjtuprog/fox-news-comments
- JSON file, the posts are there, so the dataset might be useful

### Are You a Racist or Am I Seeing Things?
[data directory](data/are_you_a_racist_or_am_i_seeing_things)

- English
- Twitter
- 4,033
- Multi-topic (Sexist, Racist, Neither, Both)
- paper: https://www.aclweb.org/anthology/W16-5618.pdf
- github: https://github.com/zeerakw/hatespeech
- only Twitter IDs

### When Does a Compliment Become Sexist?
[data directory](data/when_does_a_compliment_become_sexist)

- English
- Twitter
- 712
- Hierarchy of Sexism (Benevolent sexism, Hostile sexism, None)
- paper: https://www.aclweb.org/anthology/W17-2902.pdf
- github: https://github.com/AkshitaJha/NLP_CSS_2017
- only Twitter IDs

### Overview of the Task on Automatic Misogyny Identification at IberEval 2018
[data directory](data/overview_of_the_task_an_automatic_misogyny_identification_at_ibereval_2018)

- English
- Twitter
- 3,977
- Binary (misogyny / not), 5 categories (stereotype, dominance, derailing, sexual harassment, discredit), 
  target of misogyny (active or passive)
- paper: http://personales.upv.es/prosso/resources/FersiniEtAl_IberEval18.pdf
- github: https://github.com/MIND-Lab/ami2018
- filled out a form to get the dataset, waiting for e-mail reply on how to download the data

### CONAN -COunter NArratives through Nichesourcing
[data directory](data/conan)

- English
- Synthetic/Facebook posts
- 1,288
- Binary (Islamophobic / not), multi-topic (Culture, Economics, Crimes, Rapism, Terrorism, Women 
  Oppression, History, Other/generic)
- paper: https://www.aclweb.org/anthology/P19-1271.pdf
- github: https://github.com/marcoguerini/CONAN
- JSON file, well documented dataset
  
**File description*:*

In the json file, each line starts with an ID, followed by a pair of hate speech/counter-narrative  
and the metadata (hate speech type, hate speech sub-topic, counter-narrative type, and demographics).

ID indicates language, hate speech type, hate speech sub-topic, unique hate speech count, 
counter-narrative count, and augmentation type (if any).

### Characterizing and Detecting Hateful Users on Twitter

- English
- Twitter
- 4,972
- Binary(hateful/not)
- paper: https://arxiv.org/pdf/1803.08977.pdf
- github: https://github.com/manoelhortaribeiro/HatefulUsersTwitter 
- data (on Kaggle): https://www.kaggle.com/manoelribeiro/hateful-users-on-twitter?select=users.edges; didn't put in 
  separate data folder, because too large, but I think it's again only Twitter IDs
  
  
### A Benchmark Dataset for Learning to Intervene in Online Hate Speech
[data_directory](data/gab_binary-jing-qian)

- English
- Platform Gab, posts
- 33,776
- Binary (hateful/not)
- paper: https://arxiv.org/pdf/1909.04251.pdf
- github: https://github.com/jing-qian/A-Benchmark-Dataset-for-Learning-to-Intervene-in-Online-Hate-Speech


### Multilingual and Multi-Aspect Hate Speech Analysis
[data_directory](data/multilingual_and_multi-aspect_hate_speech_analysis)

- English
- Twitter
- 5,647
- Hostility, Directness, Target attribute and Target group
- paper: https://arxiv.org/pdf/1908.11049.pdf
- github: https://github.com/HKUST


### Exploring Hate Speech Detection in Multimodal Publications

- English
- Twitter
- 149,823
- Six primary categories (No attacks to any community, Racist, Sexist, Homophobic, Religion based attack, Attack to other community)
- paper: https://arxiv.org/pdf/1910.03814.pdf
- Dataset on kaggle (6.1 GB): https://www.kaggle.com/victorcallejasf/multimodal-hate-speech


### Predicting the Type and Target of Offensive Posts in Social Media

- English
- Twitter
- 14,100
- Branching structure of tasks: Binary (Offensive, Not), Within Offensive (Target, Not), Within Target (Individual, Group, Other)
- paper: https://arxiv.org/pdf/1902.09666.pdf
- The data is retrieved from social media and distributed in comma separated format. More information will be available soon.
  
  
### hatEval, SemEval-2019 Task 5: Multilingual Detection of Hate Speech Against Immigrants and Women in Twitter

- English
- Twitter
- 13,000
- Branching structure of tasks: Binary (Hate, Not), Within Hate (Group, Individual), Within Hate (Agressive, Not)
- paper: https://iris.unito.it/retrieve/handle/2318/1723924/512658/S19-2007.pdf
- github: https://github.com/msang/hateval
- In order to get the HatEval official dataset, please fill in the form on http://hatespeech.di.unito.it/hateval.html


### Peer to Peer Hate: Hate Speech Instigators and Their Targets

- English
- Twitter
- 27,330
- Binary (Hate/Not), only for tweets which have both a Hate Instigator and Hate Target
- paper: https://arxiv.org/pdf/1804.04649.pdf
- data TweetIds on https://github.com/mayelsherif/hate_speech_icwsm18


### Overview of the HASOC track at FIRE 2019: Hate Speech and Offensive Content Identification in Indo-European Languages

- English
- Twitter and Facebook
- 7,005
- Branching structure of tasks. A: Hate / Offensive or Neither, B: Hatespeech, Offensive, or Profane, C: Targeted or Untargeted


## Additional datasets:
[data directory](data/personal_attacks_seen_at_scale_wulczyn)
- https://www.kaggle.com/c/detecting-insults-in-social-commentary/data?select=impermium_verification_labels.csv