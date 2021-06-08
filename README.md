### Text Analyzer

Describe: wordCounter()

Test: "It should return 1 if a passage has one word."
Code: 
  const text = 'Hello'
  wordCounter(text);
Expected Output: 1

Test: "It should return 2 if a passage has two words."
Code:
  const text = "Hello world"
  wordCounter(text);
Expected Output: 2  

Test: "It should return 0 for an empty string."
Code: 
  wordCounter("");
Expected Output: 0

Test: "It should not count numbers as words."
Code:
  wordCounter("hello number 2");
Expected Output: 2



Describe: numberOfOccurrencesInText()

Test: "It should return a value of 0 if there is no text."
Code:
  const text = ""
  const word = "red"
  numberOfOccurrencesInText(word, text);
Expected Output: 0

Test: "It should return 1 occurrence of a word when the word and the text are the same."
Code:
  const text = 'red';
  const word = 'red';
  numberOfOccurencesInText(word, text);
Expected Output: 1

Test: "It should return 0 occurrences of a word when the word and the text are different."
Code:
const text = "red";
const word = "blue";
numberOfOccurrencesInText(word, text);
Expected Output: 0

Test: "It should count how many times a word appears in a passage."
Code: 
  const text = "red blue red red red green"
  const word = "red"
  numberOfOccurrencesInText(word, text)
Expected Output: 4

Test: "It should return a word match regardless of case."
Code:
  const text = "red RED RED blue"
  const word = "red"
  numberOfOccurrencesInText(word, text)
Expected Output: 3

Test: "It should return a word match regardless of punctation."
Code:
  const text = "Red! red. RED?"
  const word = 'red'
  numberOfOccurrencesInText(word, text)
Expected Output: 3

Test: "If an empty string is passed in as a word, it should return 0."
Code:
  const text = "The text passage went to the text analyzer to get a text-up."
  const word = ""
  numberOfOccurrencesInText(word,text)
Expected Output: 0




Describe: boldPassage()

Test: "It should return a non-matching word in a p tag."
Code:
const word = "hello";
const text = "yo";
boldPassage(word, text);
Expected Output: "<p>yo</p>"

Test: "It should return a matching word in a b tag."
Code:
const word = "hello";
const text = "hello";
boldPassage(word, text);
Expected Output: "<p><b>hello</b></p>"

Test: "It should wrap words that match in `b` tags but not words that don't."
Code:
const word = "hello";
const text = "hello there";
boldPassage(word, text);
Expected Output: "<p><b>hello</b> there</p>"