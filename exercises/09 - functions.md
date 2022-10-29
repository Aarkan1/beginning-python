## Exercise 9: functions

Rövarspråket (English: The Robber Language) is a Swedish language game. 

The formula for encoding is simple. Every consonant (spelling matters, not pronunciation) is doubled, and an o is inserted in-between. Vowels are left intact. It is possible to render the Rövarspråket version of an English word as well as a Swedish, such as the following for the word stubborn:

`sos-tot-u-bob-bob-o-ror-non` or `sostotubobboborornon`

1. Create a function that takes `text` as an argument, and returns the text encoded to Rövarspråket. 

  `"This is a swedish game!"` should return:

  `"Tothohisos isos a soswowedodisoshoh gogamome!"`

2. Now create another function to decode a `text` argument from Rövarspråket back to it's original text.  

  `"Hohinontot, sosololvove tothohisos wowitothoh a wowhohilole loloopop"` should return:
  
  `"Hint, solve this with a while loop"`
