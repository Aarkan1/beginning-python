## Exercise 9: functions

> 1. Create a function that takes `text` as an argument, and returns the text encoded to Rövarspråket.

Remember that we can loop a string like a list?

Here I used a string of consonants to check if the current character is part of that string.

```py
def robber_encode(text):
    consonants = "bcdfghjklmnpqrstvwxz"

    result = ""

    for char in text:
        if char in consonants:
            result += f"{char}o{char}"
        else:
            result += char

    return result

robber_text = robber_encode("This is a swedish game!")
print(robber_text)
```

Result

```txt
Thohisos isos a soswowedodisoshoh gogamome!
```

At a first glance this looks right, but look closely at the first word.
`Thohisos` should be `Tothohisos`.
The function doesn't handle upper case characters when matching against the consonants.

Solve this by adding `.lower()` to the char in the if statement.

```py
if char.lower() in consonants:
```

Now the result is

```txt
ToThohisos isos a soswowedodisoshoh gogamome!
```

Still not there yet. The second occurrence the the character should be lower case. `ToT` should be `Tot`.

To solve this we simply add `.lower()` to the second char when adding to result.

```py
result += f"{char}o{char.lower()}"
```

Final result

```txt
Tothohisos isos a soswowedodisoshoh gogamome!
```

> 2. Now create another function to decode a `text` argument from Rövarspråket back to it's original text.

```py
def robber_decode(text):
    consonants = "bcdfghjklmnpqrstvwxz"

    result = ""

    i = 0
    while i < len(text):
        char = text[i]

        result += char

        if char.lower() in consonants:
            i += 2

        i += 1

    return result

decoded_robber_text = robber_decode("Hohinontot, sosololvove tothohisos wowitothoh a wowhohilole loloopop")
print(decoded_robber_text)
```

Result

```txt
Hint, solve this with a while loop
```
