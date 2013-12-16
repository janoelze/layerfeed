# Layerfeed Specification
## Version 0.1

### 1. Abstract

The Layerfeed standard is a file format designed to release subtitle-like text data for video files in a simple and manageable package.

### 2. Specification

* An Layerfeed file is a normal plain text file containing JSON-structured data.
* Layerfeed files end with a ".layer" extension.
* Layerfeed files needs to include the following fields:
  * ```title``` - A title for your Layerfeed.
  * ```identifier``` - This identifier field must contain a string that uniquely identifies your Layerfeed file. We recommend using [UTI format](http://en.wikipedia.org/wiki/Uniform_Type_Identifier).
  * ```version``` - The version of your Layerfeed.

#### Example Layerfeed

The following snippet shows an example layerfeed containing one layer item.

```
{
   "version":2,
   "license":"",
   "creator":["John Doe"],
   "title":"Pulp Fiction Trivia",
   "date": "2011-08-23",
   "identifier":"de.janoelze.pulp-fiction-trivia",
   "data":[
      {
         "frames":{
            "start":16500,
            "end":20500
         },
         "text":{
            "title":"Trivia",
            "body":"The bridge in the background of this scene later collapsed, due to a heavy camera car."
         },
         "actions":[
            {
               "url":"http://www.imdb.com/title/tt0087332/trivia/432908/comment",
               "text":"Comment"
            },
            {
               "url":"http://www.twitter.com/post/",
               "text":"Share"
            }
         ]
      }
   ]
}
```

### Handling layerfeed versions
