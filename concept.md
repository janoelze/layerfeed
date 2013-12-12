# Layerfeed
### A system to enrich video with timestamped textual data.

This document outlines a simple specification of the Layerfeed system.

## Contributors

- Jan Oelze
- Jathavan Sriram

## Abstract
## Introduction
## Structure of a Layerfeed

A Layerfeed consists of one or more text elements.

```
{
   "version":1,
   "title":"Pulp Fiction Trivia",
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

#### Required Fields
#### Usage

## Matching layerfeeds to video files
## Examples
## Conclusion
## References
