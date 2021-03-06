Code for "Ranking Based Multi-Label Classification for Sentiment Analysis" LKE 2019(7th International Symposium on Language & Knowledge Engineering).

### Steps to run

1. Download datasets

   * Ren_CECps dataset, download it by contacting `ren@is.tokushima-u.ac.jp`.
   * [SemEval2007](https://web.eecs.umich.edu/~mihalcea/affectivetext/).
   * Sina Social News dataset, download it by contacting `yyang@seu.edu.cn`.

   Unzip these datasets in `data` folder and use the `parser.py` to convert them into `.json` format.

   ```bash
   mkdir data && cd data
   # unzip the datasets in `data`
   python3 parser.py
   ```

2. Download pretrained model

   ```bash
   mkdir models && cd models
   mkdir bert-base-chinese && cd bert-base-chinese
   wget https://s3.amazonaws.com/models.huggingface.co/bert/bert-base-chinese.tar.gz
   tar -zxvf bert-base-chinese.tar.gz
   wget https://s3.amazonaws.com/models.huggingface.co/bert/bert-base-chinese-vocab.txt
   cd ..
   mkdir bert-base-uncased && cd bert-base-uncased
   wget https://s3.amazonaws.com/models.huggingface.co/bert/bert-base-uncased.tar.gz
   tar -zxvf bert-base-uncased.tar.gz
   wget https://s3.amazonaws.com/models.huggingface.co/bert/bert-base-uncased-vocab.txt
   ```

3. Train the model

   ```bash
   python3 bert_classifier.py
   ```

### References

* [Pytorch-transformers](https://github.com/huggingface/pytorch-transformers)

* [Sentence emotion analysis and recognition based on emotion words using ren-cecps](https://www.researchgate.net/publication/229049748_Sentence_Emotion_Analysis_and_Recognition_Based_on_Emotion_Words_Using_Ren-CECps)

* [Relevant Emotion Ranking from Text Constrained with Emotion Relationships](https://www.researchgate.net/publication/325449027_Relevant_Emotion_Ranking_from_Text_Constrained_with_Emotion_Relationships)
