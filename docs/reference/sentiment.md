# Sentiment


<center>
    <img style="display:block; max-height:20rem" alt="image classification of bird" src="https://via.placeholder.com/150">
</center>


## Description

Sentiment is a model trained to predict the sentiment of any given text. The default model, currently 'moviereviews', is trained using IMDB reviews that have been truncated to a maximum of 200 words, only the 20000 most used words in the reviews are used.

## Quickstart

```js
// Create a new Sentiment method
const sentiment = ml5.sentiment('movieReviews', modelReady);
      
// When the model is loaded
function modelReady() {
  // model is ready
  console.log("Model Loaded!");
}

// make the prediction
const prediction = sentiment.predict(text);
console.log(prediction);
```


## Usage

### Initialize

```js
const magic = ml5.Sentiment(model, ?callback )
```

#### Parameters
* **model**: REQUIRED. Defaults to 'moviereviews'. You can also use a path to a `manifest.json` file via a relative or absolute path.
* **callback**: OPTIONAL. A callback function that is called once the model has loaded. If no callback is provided, it will return a promise that will be resolved once the model has loaded.


### Properties

***
#### .ready
> Boolean value that specifies if the model has loaded.
***

***
#### .model
> The model being used.
***


### Methods


***
#### .predict()
> Given a number, will make magicSparkles

```js
sentiment.predict(text)
```

📥 **Inputs**

* **text**: Required. String. A string of text to predict 


📤 **Outputs**

* **Object**: Scores the sentiment of given text with a value between 0 ("negative") and 1 ("positive").

***


## Examples

**plain javascript**
* [Sentiment_Interactive]()

**p5.js**
* [Sentiment_Interactive]()

**p5 web editor**
* [Sentiment_Interactive]()

## Demo

No demos yet - contribute one today!

## Tutorials

No tutorials yet - contribute one today!


## Acknowledgements

**Contributors**:
  * Name 1
  * Name 2

**Credits**:
  * Paper Reference | Website URL | Github Repo | Book reference | etc


## Source Code

[/src/Sentiment/](https://github.com/ml5js/ml5-library/tree/release/src/Sentiment)

