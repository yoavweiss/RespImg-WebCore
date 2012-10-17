steps towards a working picture element
--------------------
* HTMLPictureElement: public HTMLImageElement
* Should also inherit lots of functionality from HTMLMediaElement. Not
  yet sure how
* What do we want to do with ImageInnerElement? Should we duplicate a
  similar one as HTMLPictureElement's shadow DOM, and can we use it as is?
* Add handling of <picture> tag to the PreloadScanner
 - need to look for <source> and load them according to media
* How can I do media queries eval inside the preload scanner?
  MediaQueryMatcher? All I need to get started is get the window
dimensions from somewhere... 
* How can I scan source tags with the preload scanner?
