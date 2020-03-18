**Implementation details**

This implementation shows how to implement the use case described in the question: [How to get a value ($item.xxx) from a Link Widget into a collection as URL Parameter](https://community.bonitasoft.com/questions-and-answers/how-get-value-itemxxx-link-widget-collection-url-parameter)

It has been implemented with Bonita 7.10.3 Community Edition:

Variables:  
cases (JSON) : [{"id":"123"},{"id":"456"}]  

Container:  
collection: cases  

Link widget:  
URL: "http://..../UserDetails?" + $item.id  
