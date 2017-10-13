# Universal Regex Search Results

## Description

*Universal Regex Search Results* (URSR) is a format to store regex search results.

## What is this good for?

This format is a possible communication basis for a new generation of search (and replace) tools which are build around regular expressions.


## URSR in JSON:

```json
{
  "ref": "/home/peter/example.txt",
  "type": "file",
  "encoding": "utf-8",
  "pattern": "foo",
  "matches": [
    {
      "before": "Context before match...",
      "match": "hello",
      "replace": "bye",
      "after": "Context after match...",
      "groups": ["Regex capture group val1.", "Regex capture group val2"],
      "start": 8924,
      "len": 5,
      "line": 590,
      "col": 42
    },
    {
      "Next Match":"..."
    }
  ]
}
```

                         UXRXTZ    

## Header

The header contains information about the reference and the search that was performed.

#### `ref`


The reference that was searched. Can be a file path, an url or the search 
reference itself as a string.

#### `type`

The reference type. Can be 'file', 'url', 'string', etc.

#### `encoding`

The encoding of the reference.

#### `pattern`

The pattern that was used to perform the search. (Usually a regex pattern)

#### `matches`

A list of matches see Match below. 


## Matches

Each URSR main contain multiple *Matches*.

#### `before`

Context before the match. (optional)

#### `match`

The value that matches the search pattern.

#### `repl`

A replacement for the 'match'. (optional)

#### `after`

Context after the match. (optional)

#### `groups`

Regex capture group values.

#### `start`

The starting position of the match, within the reference.

#### `len`

The length of the match.

#### `line`

The line number in which the match starts.

#### `col`

The column in which the match starts.



