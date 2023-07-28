# Reading Task

I have selected the paper _A Survey of Computational Framing Analysis Approaches_ for this task.

A pdf with important sections highlighted can be found here - https://drive.google.com/file/d/1i2V8ni7k7w86eicxgpyxB_73mM24oP2L/view?usp=sharing.

## About the paper

I chose this paper as I believe that it can help with the task of analyzing frames which is a very important task during elections.

### What is Frame?

A very important aspect of framing is that it allows one to focus on a specific aspect of a matter while completely alienating other related things. It is based on context and is shaped by
1. Texts,
2. Communicators,
3. Receivers, and, 
4. Cultures

Identifying the _framing devices_ (that which make some part of the information stand out) is crucial. They fall into 4 groups:
1. Content
2. Action
3. Context
4. Communicator

### Approaches

1. Codebook and corpora approaches
- PFC and MFC
    - 15 dimensions were predetermined and not evolving.
    - The dimensions were topics and not frames - they didn't consider that the phrasing of a sentence can subtly change its meaning.
- GVFC
    - Defined some frames, manually annotated and then run BERT
    - Not all framing codes were defined to capture all nuances of frames.

2. Computational Approaches
- Topic Modeling (TM)
    - Conceptualized frames well but the output didn't align with their idea as they used lists of words which do not yield semantics
    - Once again yielded topics but not frames
- Structural TM
    - Included metadata which gives some more context than just TM
    - But inherently flawed due to BOW approach
- Hierarchical TM
    - Gives two levels of nodes (Agendas with frames as children)
    - However the idea of taking frames to be equivalent to sub-agendas doesn't align with the general definition of frames
- Cluster Analysis
    - Conceptualized frames in terms of word frequencies which constitutes only a fourth of all the framing devices.
    - Goes against the idea that a framing device belongs to multiple frames
- Neural Network Model
     - Based on transfer learning
     - Might have been really good if not for bas choice of datasets (MFC and GVFC)
- Parsing Semantic Relations
     - More innovative as it considers semnatics as well 
     - Did not adequately exploit nuances of frames
- Frequency Based Model
    - Defined frame in terms of word recurrence
    - Did not conceptualize frames adequately
- FrameAxis
    - Based on antonyms
    - Limited due to its base but can identify whether some some bits of the information are made more salient 
- ANTMN
    - Can analyze emphasis frames but not equivalency frames
    - Used idea that a frame repeatedly invokes the "same objects and traits, using identical or synonymous words and symbols..." (page 8)
    - No evidence to support equivalence between communities and frames
    
### Major challenge
Current NLP technologies can't understand nuances behind "how" a sentence is framed.
    
## Improvements and Elections 2024

- Most of the data expressed by individuals on the internet are usually highly polarised. Thus, using FrameAxis for its advantage of understanding antonyms and highlighted information can be useful. ANTMN also has the same advantages.
    - This can prove useful to analyse the effects of polictial advertising among different age groups as political advertising usually contains emphasis frames.
    - It can also be used to gain insights on the various different view points on a topic on the internet. For example, after a major accident multiple parties will be promoting different parts of the whole truth.

- Neural networks suffer from not having a good dataset to train on. A corpus on politics can prove to be better than the existing datasets but will also suffer from pre-determined topics.

- Although we are restricted to using only words as framing devices most of the data available for politics isn't affected by "how" the sentences are framed. Opinions available on the internet are usually skewed towards one side. 

- Most of these methods focus on addressing only headlines. However, headlines often miss context. So, we can inspect entire articles instead of just headlines to give more importance to words repeated from the main article within the headline or concluding paragraph.

- Frequency based methods can be combined with position and word embeddings to get a better understanding of the semantics of the sentence. Community detection algorithms similar to ANTMN can be used to cluster post this.

- Given a number of articles, we compare their semantic similarities by running a pre-trained model on the _summaries_ of the articles. Word frequencies can be analyzed to give the list of most repeated significant words using a pre-trained model once again. Run clustering algorithm on this list to find how different groups of articles are related to each other. This could be a new direction of investigation.

- We can add metadata about the communicator, receivers and location to political data and then run Structured TM to get a few insights.

- Hierarchical TM can be used to take political parties as topics and sub-agendas as their beliefs.

- Responses to a given piece of information can be understood using sentiment analysis methods to better understand the phrasing of the initial information.