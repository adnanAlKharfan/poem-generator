# poem generator

This repository shows how to make a poem generator model using advance AI ideas.

## Introduction 

The poem generator model objective to generate a poem following the styles it trained on to show AI creativity and art in poem creation. 

## Dataset

The poet robert frost poems were used in this model to see if AI could follow the style of the poet and generalize on it.

### Example of the data:

- `whose woods these are i think i know.
   his house is in the village though;
   he will not see me stopping here
   to watch his woods fill up with snow.
   my little horse must think it queer
   to stop without a farmhouse near
   between the woods and frozen lake
   the darkest evening of the year.
   he gives his harness bells a shake
   to ask if there is some mistake.
   the only other sound’s the sweep
   of easy wind and downy flake.
   the woods are lovely, dark and deep,
   but i have promises to keep,
   and miles to go before i sleep,
   and miles to go before i sleep.`


## Methodology

I used pretrained glove 50 dimension for embedding layers weight, i took the input as from the first word to minimum length of any sentence and the output is the word after it, then the output of the embedding layer get passed with the states of previous lstm to the LSTM layer with return state enabled, the output of the LSTM is passed to dense layer with number of all words as its number of output with softmax function as the layer activation function. category cross entropy used as loss function since softmax was used and accuracy as a metric with adam as the model optimizer.

## Experiment

- Epochs: `10`
- Batch size: `32`
- Validation split: `0.2`
- Accuracy: `0.9519`
- Loss: `0.3090`
- Validation Accuracy: `0.9020`
- Validation Loss: `0.7973`

## Result

- `weary, has rough is;
the 
baptiste bells`

## Contributing

Contributions are welcome! If you have any improvements or new features you would like to add, please submit a pull request.
