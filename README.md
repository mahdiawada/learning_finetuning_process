# learning_finetuning_process
In this repository I will be showing my learning process in learning finetuning.

First Step: Define our use case
We want to fine-tune a model, which can generate SQL queries bases on a natural language instruction, which can them be integrated into our web interface. The goal is to reduce the time it takes to create a SQL query and make it easier for non-technical users to create SQL queries.

Second Step: Setup the development enviroment
We will install Hugging Face Libraries and Pytorch, including trl, transformers and datasets.
trl is a new library on top of transformers and datasets, which makes it easier to fine-tune, rlhf(Reinforcement Learning from Human Feedback), align open LLMs.
And for sure we will use the Hugging Face Hub to login into hugging face account

Third Step: Create and prepare the dataset
We need to create a dataset to fine-tune our model.
We will use existing open-source datasets (ex:Spider)
Depending on our use case we will use an already existing dataset called sql-create-context, which containes samples of natural language instructions, schema definitions and the corresponding SQL query.
Now we need to convert out dataset to one of the supported formats and `trl` will take care of the rest, it includes two types of formats conversational format and instruction format.


