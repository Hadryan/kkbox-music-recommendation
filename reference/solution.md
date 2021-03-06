## 1

https://www.kaggle.com/c/kkbox-music-recommendation-challenge/discussion/45942

### Model

> 0.6 * LightGBMs + 0.4 * NNs; this ensemble gives about 0.004 boost over LightGBMs alone.

### Code

https://github.com/lystdo/Codes-for-WSDM-CUP-Music-Rec-1st-place-solution

## 3

https://www.kaggle.com/c/kkbox-music-recommendation-challenge/discussion/45971

### Preprocess

1. Join interaction (train, test) table with user, item (song) table.
2. Fill missing data points.

### Model

XGBoost and CatBoost.

### Features

1. mean of target from history by categorical features (pairs and triples)
2. count – the number of observations in all data by categorical features (pairs and triples)
4. time_from_prev_heard – time from last heard by categorical features (msno, msno + genre_ids, msno+composer and so on)
5. time_to_next_heard – time to next heard by categorical features (pairs and triples which include msno)
6. last_time_diff – time to the last heard by categorical features
7. part_of_unique_song – the share of unique song of artist that the user heard on all unique song of artist
3. regression – linear regression target by categorical features (msno, msno + genre_ids, msno+composer and so on)
8. matrix_factorization – LightFM. I use as a user msno in different context (source_type) and the msno was the feature for user.

### Code

https://github.com/VasiliyRubtsov/wsdm_music_recommendations/blob/master/pipeline.ipynb

## 6

https://www.kaggle.com/c/kkbox-music-recommendation-challenge/discussion/45999

## 7

https://www.kaggle.com/c/kkbox-music-recommendation-challenge/discussion/45614

