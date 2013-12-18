# Layerfeed Specification
## Version 0.1

### Abstract

The Layerfeed standard is a file format designed to release subtitle-like text data for video files in a simple and manageable package.

### License

This document is distributed under a Creative Commons Attribution-ShareAlike license. For details, see:

http://creativecommons.org/licenses/by-sa/3.0/

### Goals / Rationale

Current subtite formats lack sophisticated features like in-text hotlinks or providing x and y coordinates to position text on screen.

(...)

We aim to design Layerfeed in a way that enables individuals to enrich videos with timestamped textual data. Layerfeed tries to encourage individuals to create creative and new content. 

### Specification

* An Layerfeed file is a normal plain text file containing JSON-structured data.
* Layerfeed files end with a ".layer" extension.
* Layerfeed files needs to include the following fields:
  * ```title``` - A title for your Layerfeed.
  * ```identifier``` - This identifier field must contain a string that uniquely identifies your Layerfeed file. We recommend using [UTI format](http://en.wikipedia.org/wiki/Uniform_Type_Identifier).
  * ```version``` - The version of your Layerfeed.

#### Outline

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
### Handling layerfeed to video matching
### Displaying 

![](https://s3-eu-west-1.amazonaws.com/51e3d489f1e/2013-12-18-06-02-08-52b12c50db205.png)
