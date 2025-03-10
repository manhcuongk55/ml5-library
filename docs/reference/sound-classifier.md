# SoundClassifier


<center>
    <img style="display:block; max-height:20rem" alt="image classification of bird" src="https://via.placeholder.com/150">
</center>


## Description

The ml5.soundClassifier() allows you to classify audio. With the right pre-trained models, you can detect whether a certain noise was made (e.g. a clapping sound or a whistle) or a certain word was said (e.g. Up, Down, Yes, No). At this moment, with the ml5.soundClassifier(), you can use your own custom pre-trained speech commands or use the the "SpeechCommands18w" which can recognize "the ten digits from "zero" to "nine", "up", "down", "left", "right", "go", "stop", "yes", "no", as well as the additional categories of "unknown word" and "background noise"."

## Quickstart

```js
// Options for the SpeechCommands18w model, the default probabilityThreshold is 0
const options = { probabilityThreshold: 0.7 };
const classifier = ml5.soundClassifier('SpeechCommands18w', options, modelReady);

function modelReady() {
  // classify sound
  classifier.classify(gotResult);
}

function gotResult(error, result) {
  if (error) {
    console.log(error);
    return;
  }
  // log the result
  console.log(result);
}
```


## Usage

### Initialize

```js
const soundclassifier = ml5.soundClassifier(?model, ?options, ?callback)
```

By default the soundClassifier will start the default microphone.

#### Parameters
* **model**: Optional. Model name or URL path to a `model.json`
* **callback**: Optional. A function to run once the model has been loaded.
* **options**: Optional. An object describing a model accuracy and performance. The available parameters are:
  
    ```
    {
     probabilityThreshold: 0.7 // probabilityThreshold is 0
    }
    ```

### Properties


***
#### .model
> *Object*. The model.
***


### Methods


***
#### .classify()
> Given a number, will make magicSparkles

```js
soundclassifier.classify(callback);
```

📥 **Inputs**
* **callback**: A function to handle the results of the classification

📤 **Outputs**
* **Array**: Returns an array with "label" and "confidence".

***




## Examples

**plain javascript**
* [SoundClassification_speechcommand]()
* [SoundClassification_speechcommand_load]()


**p5.js**
* [SoundClassification_speechcommand]()
* [SoundClassification_speechcommand_load]()

**p5 web editor**
* [SoundClassification_speechcommand]()
* [SoundClassification_speechcommand_load]()

## Demo

No demos yet - contribute one today!

## Tutorials

### ml5.js: Sound Classification via CodingTrain
<iframe width="560" height="315" src="https://www.youtube-nocookie.com/embed/cO4UP2dX944" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

## Acknowledgements

**Contributors**:
  * Name 1
  * Name 2

**Credits**:
  * Paper Reference | Website URL | Github Repo | Book reference | etc




## Source Code

* [/src/SoundClassifier/](https://github.com/ml5js/ml5-library/tree/release/src/SoundClassifier)
