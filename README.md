# NTI 2021 AI finals
## Task: RuCoS *(Russian reading comprehension with Commonsense reasoning)*, [link](https://russiansuperglue.com/tasks/task_info/RuCoS)
**A solutions for [NTI Contest](https://onti2020.ai-academy.ru) by [@otter18](https://github.com/otter18) & [@MichailKon](https://github.com/MichailKon)**

## *All submits are linked with notebooks by random hash*

## Solutions
- [`wbwpk9e9zr.ipynb`](https://github.com/otter18/nti-2021-ai-final/blob/main/13ut5xrhvr.ipynb) - bert *(public score: 0.8153)*
    * model_name = "DeepPavlov/rubert-base-cased"
    * num_train_epochs = 2 
    * learning_rate =  3e-5 
    * train_batch_size = 32 
    * adam_epsilon =  3e-8
   
- [`13ut5xrhvr.ipynb`](https://github.com/otter18/nti-2021-ai-final/blob/main/wbwpk9e9zr.ipynb) - bert *(public score: None)*
    * model_name = "DeepPavlov/rubert-base-cased"
    * num_train_epochs = 2 
    * learning_rate =  5e-5 
    * train_batch_size = 32 
    * adam_epsilon =  3e-8

## Tools developed for this project
- `tg_logger` *(useful for Google Colab because it resets the VM frequently)*, [[pypi]](https://pypi.org/project/tg-logger/), [[repo]](https://github.com/otter18/tg_logger)
