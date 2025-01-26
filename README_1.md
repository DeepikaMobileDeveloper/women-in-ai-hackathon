#Dataset
Rebrickables
https://rebrickable.com/downloads/
![alt text](image-2.png)

#Pre-processing
Form the dataset by running Depth First Search on the dataframes built from the CSVs
For each lego set, build a combined string of part descriptions

#Embedding Vectors
Generate embeddings for the set and part description strings using Sentence Transformers
['all-MiniLM-L6-v2'](https://huggingface.co/sentence-transformers/all-MiniLM-L6-v2) model was used to generate the vector embeddings
A Milvus collection was created for the LEGO data and loaded into to a Zilliz cluster
![alt text](image-1.png)

