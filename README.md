# NTI 2021 AI finals
## Task: RuCoS *(Russian reading comprehension with Commonsense reasoning)*, [link](https://russiansuperglue.com/tasks/task_info/RuCoS)
**A solutions for [NTI Contest](https://onti2020.ai-academy.ru) by [@otter18](https://github.com/otter18) & [@MichailKon](https://github.com/MichailKon)**

## *All submits are linked with notebooks by random hash*
## Scores

Hash | Type| Public score
--- | --- | ---
[`wbwpk9e9zr`](https://github.com/otter18/nti-2021-ai-final/blob/main/13ut5xrhvr) | DeepPavlov/rubert-base-cased | 0.8153
[`13ut5xrhvr`](https://github.com/otter18/nti-2021-ai-final/blob/main/wbwpk9e9zr) | DeepPavlov/rubert-base-cased | None
[`p871faksle`](https://github.com/otter18/nti-2021-ai-final/blob/main/p871faksle) | RuBERT | None
[`jndykzt1i7`](https://github.com/otter18/nti-2021-ai-final/blob/main/jndykzt1i7) | DeepPavlov/rubert-base-cased | None
[`66me00urb3`](https://github.com/otter18/nti-2021-ai-final/blob/main/66me00urb3) | catboost + cosine_similarity | 0.243
[`wbwpk9e9zr`](https://github.com/otter18/nti-2021-ai-final/blob/main/13ut5xrhvr) | official baseline | 0.1281



## Solutions
- [`wbwpk9e9zr`](https://github.com/otter18/nti-2021-ai-final/blob/main/13ut5xrhvr) - bert *(public score: 0.8153)*
    ```python3
    model_name = "DeepPavlov/rubert-base-cased"
    num_train_epochs = 2 
    learning_rate =  3e-5 
    train_batch_size = 32 
    adam_epsilon =  3e-8
    ```

- [`13ut5xrhvr`](https://github.com/otter18/nti-2021-ai-final/blob/main/wbwpk9e9zr) - bert *(public score: None)*
    ```python3
    model_name = "DeepPavlov/rubert-base-cased"
    num_train_epochs = 2 
    learning_rate =  5e-5 
    train_batch_size = 32 
    adam_epsilon =  3e-8
   ```

- [`p871faksle`](https://github.com/otter18/nti-2021-ai-final/blob/main/p871faksle) - bert *(public score: None)*
    ```python3
    model_name = "RuBERT/"
    num_train_epochs = 2 
    learning_rate =  5e-5 
    train_batch_size = 32 
    adam_epsilon =  3e-8
   ```

- [`jndykzt1i7`](https://github.com/otter18/nti-2021-ai-final/blob/main/jndykzt1i7) - bert *(public score: None)*
    ```python3
    model_name = "DeepPavlov/rubert-base-cased"
    num_train_epochs = 2 
    learning_rate =  1e-4
    train_batch_size = 32 
    adam_epsilon =  3e-8

- [`66me00urb3`](https://github.com/otter18/nti-2021-ai-final/blob/main/66me00urb3) - catboost + cosine_similarity *(public score: 0.243)*
    ```python3
    learning_rate = 1e-2
    max_depth = 4
    iterations = 1000
    loss_function = "MultiClass"
    eval_metric = 'MultiClass'
    random_seed = 179
    ```

- [`9kv9df5nkbbh0tjt`](https://github.com/otter18/nti-2021-ai-final/blob/main/9kv9df5nkbbh0tjt) - official baseline *(public score: 0.1281)*
    * tfidf_baseline


## Tools developed for this project
- `tg_logger` *(useful for Google Colab because it resets the VM frequently)*, [[pypi]](https://pypi.org/project/tg-logger/), [[repo]](https://github.com/otter18/tg_logger)
