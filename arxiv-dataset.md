# arXiv Dataset

## Download Data

Metadata download [here](https://www.kaggle.com/datasets/Cornell-University/arxiv?resource=download)


To download PDFs, use this command:

```bash
gsutil -m cp -r gs://arxiv-dataset/arxiv/arxiv/pdf/2401 ./pdf/
```

This command will download papers from year *(20)24* and month *01*. I downloaded all years from 2017-23, and found that each month contains on the order of 50GB of pdf files. For this project, I've chosen to start with 2017, because this is the year that Google researchers published the *Attention is All You Need* {cite}`vaswani_attention_2017` paper, introducing the Transfomer architecture that has led to the explosion of *Large Language Models* we see today.


## Preprocess
- arXiv has a category taxonomy here [topic](https://arxiv.org/category_taxonomy). 
- Pull out relevant papers based on topic
- Convert to parquet
- Filter to subset
- Extract text

