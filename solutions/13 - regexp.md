## Exercise 13: regular expressions

> Write a program that puts the string `"Hello this<comment1> is a <comment2>
> test"` in a variable, and then uses regular expressions to remove the comments
> from the string.

```python
>>> string_with_comments = 'Hello this<comment1> is a <comment2> test'
```

Let's first do this the wrong way, for great learning:

```python
>>> COMMENT = re.compile(r'<.*>')
>>> COMMENT.sub('', string_with_comments)
'Hello this test'
```

Oops. What happened to `'is a '`?

The problem is that the `.*` is _greedy_, and matches as much as it can. We
need to rein it in somewhat. These are two possible solution; the second one is
more specific and preferable:

```python
>>> COMMENT = re.compile(r'<.*?>')
>>> COMMENT.sub('', string_with_comments)
'Hello this is a  test'
>>> COMMENT = re.compile(r'<[^>]*>')
>>> COMMENT.sub('', string_with_comments)
'Hello this is a  test'
```
