**Implementation details**

This implementation shows how to implement the use case described in the question: [Link task in application](https://community.bonitasoft.com/questions-and-answers/link-task-application)

It has been implemented with Bonita 7.10.3 Community Edition:

Variables:  
currentUser (ExternalAPI) :../API/system/session/1   
tasklist (ExternalAPI) : ../API/bpm/humanTask?c=10&p=0&f=state=ready&f=user_id={{currentUser.user_id}}  

Container:  
collection: tasklist  

Link widget:  
Type: Human Task Form  
Task Id: $item.id  
Text: Link to {{$item.name}} form  

