[<=== Back](/README.md)

# Local Storage

[Mark Pilgrim](http://diveinto.html5doctor.com/storage.html)

[Christian Heilmann: SmashingMagazine](https://www.smashingmagazine.com/2010/10/local-storage-and-how-to-use-it/)

[Jonathan Freeman: InfoWorld](https://www.infoworld.com/article/3222851/what-is-json-a-better-format-for-data-exchange.html)

## What is JSON? A better format for data exchange
by: Jonathan Freeman
*Summarized*

> JavaScript Object Notation is a schema-less, text-based representation of structured data that is based on key-value pairs and ordered lists.

An example of data encoded in JSON:
```
{
  "firstName": "Jonathan",
  "lastName": "Freeman",
  "loginCount": 4,
  "isWriter": true,
  "worksWith": ["Spantree Technology Group", "InfoWorld"],
  "pets": [
    {
      "name": "Lilly",
      "type": "Raccoon",
    }
  ]
}
```

> A structure like the one above may be passed from a server to a web browser or a mobile application, which will then perform some action such as displaying the data or saving it for later reference. 

JSON files end with the .json extension - plain text files.

JSON allows the web browser to load content, and data to be manipulated incrementally instead of rendering a new HTML page at every event.

### JSON Drawbacks
- Easy to mis-represent data
- Only one number type available
- No date type. Dates must be represented as strings.
- No comments. Misunderstandings likely.
- Verbosity. For high-volume or special-purpose services, use more efficient data formats.

## When to use JSON

> If you're writing software the communicates with a browser or native mobile application, you should use JSON as the data format.

## JSON parser

> The part of an application's code that transforms data stored as JSON into a format the application can use is called a *parser*. JavaScript includes a native parser - the `JSON.parse()` method.

[MDN Tutorial for JSON](https://developer.mozilla.org/en-US/docs/Learn/JavaScript/Objects/JSON)