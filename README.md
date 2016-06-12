# Author/Word/Conference Representation

## Data Preprocessing
run `extraction.ipynb`, extractions are stored in `extr-titles-abstract.npy`

## Author-Word Model
use Doc2Vec model.

* Each author's research interests keywords form a sentence,
* Author is regarded as label

run `doc2vec-model.ipynb`

## Author-Conference Model
`conf_list.csv` includes 76 top conferences/journals from domains of
data ming/database/information retrieval/artificial intelligence

use DeepWalk model

* Each conference venue as _hub_ node
* Each author who published some one of paper has an edge with hub node
* random sampling walks as _sentence_, use Word2Vec to learn node (author&conference) representation

run `deepwalk-model.ipynb`
