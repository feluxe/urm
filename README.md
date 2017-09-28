# Universal Search Results

## Description

*Universal Search Results* (USR) is a format that can be used to present search results.
It's goal is to offer a standard, that applications can agree on, to exchange search results.

## USR in JSON:

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
      "start": 89243,
      "len": 5,
      "line": 61,
      "col": 42
    },
    {
      "before": "Context before match...",
      "match": "hello",
      "replace": "bye",
      "after": "Context after match...",
      "groups": ["Regex capture group val1.", "Regex capture group val2"],
      "start": 89243,
      "len": 5,
      "line": 61,
      "col": 42
    }     
  ]
}
```

### Header

`ref`


The reference that was searched. Can be a file path, an url or the search 
reference itself as a string.

`type`

The reference type. Can be 'file', 'url', 'string', etc.

`encoding`

The encoding of the reference.

`pattern`

The pattern that was used to perform the search. (Usually a regex pattern)

`matches`

A list of matches see Match below. 


### Match

`before`

Context before the match. (optional)

`match`

The value that matches the search pattern.

`repl`

A replacement for the 'match'. (optional)

`after`

Context after the match. (optional)

`groups`

Regex capture group values.

`start`

The starting position of the match, within the reference.

`len`

The length of the match.

`line`

The line number in which the match starts.

`col`

The column in which the match starts.



