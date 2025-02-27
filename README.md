# NTI 2021 AI finals

### **A solutions for [NTI Contest](https://onti2020.ai-academy.ru) by [@otter18](https://github.com/otter18) & [@MichailKon](https://github.com/MichailKon)**
### Task: RuCoS *(Russian reading comprehension with Commonsense reasoning)*, [link](https://russiansuperglue.com/tasks/task_info/RuCoS)
### *All submits are linked with notebooks by random hash*

## Scores

Hash | Type| Public score
--- | --- | ---
[`wbwpk9e9zr`](wbwpk9e9zr/) | DeepPavlov/rubert-base-cased | **0.8153**
[`ensemble`](ensemble/) | berts + catboost | None
[`13ut5xrhvr`](13ut5xrhvr/) | DeepPavlov/rubert-base-cased | 0.7947
[`p871faksle`](p871faksle/) | RuBERT | 0.5807 
[`jndykzt1i7`](jndykzt1i7/) | DeepPavlov/rubert-base-cased | 0.6575 
[`5l1p67kt4q`](5l1p67kt4q/) | DeepPavlov/rubert-base-cased | 0.8027 
[`66me00urb3`](66me00urb3/) | catboost + cosine_similarity | 0.243
[`9kv9df5nkbbh0tjt`](9kv9df5nkbbh0tjt/) | official baseline | 0.1281


## Tools developed for this project
- `tg_logger` *(useful for Google Colab because it resets the VM frequently)*, [[pypi]](https://pypi.org/project/tg-logger/), [[repo]](https://github.com/otter18/tg_logger)


## Solutions
- [`wbwpk9e9zr`](wbwpk9e9zr/) - bert *(public score: 0.8153)*
    ```python3
    model_name = "DeepPavlov/rubert-base-cased"
    num_train_epochs = 2 
    learning_rate =  3e-5 
    train_batch_size = 32 
    adam_epsilon =  3e-8
    ```

- [`ensemble`](ensemble/) - bert assembled by catboost *(public score: None)*
    * [`wbwpk9e9zr`](13ut5xrhvr/) bert
    * [`5l1p67kt4q`](5l1p67kt4q/) bert
    * some non-text features

- [`13ut5xrhvr`](13ut5xrhvr/) - bert *(public score: 0.7947)*
    ```python3
    model_name = "DeepPavlov/rubert-base-cased"
    num_train_epochs = 2 
    learning_rate =  5e-5 
    train_batch_size = 32 
    adam_epsilon =  3e-8
   ```

- [`p871faksle`](p871faksle/) - bert *(public score: 0.5807)*
    ```python3
    model_name = "RuBERT/"
    num_train_epochs = 2 
    learning_rate =  5e-5 
    train_batch_size = 32 
    adam_epsilon =  3e-8
   ```

- [`jndykzt1i7`](jndykzt1i7/) - bert *(public score: 0.6575)*
    ```python3
    model_name = "DeepPavlov/rubert-base-cased"
    num_train_epochs = 2 
    learning_rate =  1e-4
    train_batch_size = 32 
    adam_epsilon =  3e-8

- [`5l1p67kt4q`](5l1p67kt4q/) - bert *(public score: 0.8027)*
    ```python3
    model_name = "DeepPavlov/rubert-base-cased"
    num_train_epochs = 3 
    learning_rate =  4e-5
    train_batch_size = 32
    adam_epsilon =  3e-8

- [`66me00urb3`](66me00urb3/) - catboost + cosine_similarity *(public score: 0.243)*
    ```python3
    learning_rate = 1e-2
    max_depth = 4
    iterations = 1000
    loss_function = "MultiClass"
    eval_metric = 'MultiClass'
    random_seed = 179
    ```

- [`9kv9df5nkbbh0tjt`](9kv9df5nkbbh0tjt/) - official baseline *(public score: 0.1281)*
    * tfidf_baseline

