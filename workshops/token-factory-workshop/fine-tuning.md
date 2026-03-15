# Fine Tuning Models

Train the models with production inference logs we collected.

<img src="images/coninious-ai-loop.png" width="400px">


## Fine Tuning

stock model + our data --> custom model

<img src="images/fine-tuning-2.png" width="500px">

## Excercise 1: Fine tune a model

We can fine tune models right from the UI in Token Factory.

1. upload data  
   - use the dataset in `post-training/fine-tuning-1/sample-data/`.  
   - Use both `training_data.jsonl` and `validation_data.jsonl`
2. select model: `meta-llama/Llama-3.3-70B-Instruct`
3. kick off a training job
4. monitor training progress under `post training` job
5. inspect the trained model under `private` models tab
6. try out the model

See screenshots for guidance:

<kbd>
<img src="images/fine-tuning-4.png" width="300px">
</kbd>


<kbd>
<img src="images/fine-tuning-6.png" width="300px">
</kbd>


<kbd>
<img src="images/fine-tuning-5.png" width="300px">
</kbd>


## Exercise 2: Finetuning using API

checkout this [example](../../post-training/fine-tuning-1/)