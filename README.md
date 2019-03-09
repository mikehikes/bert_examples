# Interesting experiments

## bert_tpu_tweet_model.ipynb
*This notebook is designed to run in Google Colab*

This Colab notebook demonstrates the ability to conduct fast text classification using the Tensor Processing Units (TPUs) provided through Google Colab.

Using two publicly-downloadable text databases: the fivethirtyeight.com's list of Internet Research Agency's (IRA) associated tweets during the 2016 General Election in the United States, and George Washington University's database of tweets identified with the 2016 election, a BERT model will be fine-tuned and trained to determine if a tweet from these dataset is associated with the IRA (or not).

This notebook uses the BERT model checkpoints, not the TensorFlow Hub-hosted BERT models. This is because the TensorFlow Hub model uses a tf.Placeholder/feed_dict that reduces performance on TPUs and is incompatible for conducting inference. This notebook instead uses tf.Dataset with TFRecords.
