**Implementation details**

This implementation shows how to implement the use case described in the question: [Comment stocker les éléments d'une checklist dans le Data Model et ensuite l'afficher sur une page Bonita?](https://community.bonitasoft.com/questions-and-answers/comment-stocker-les-%C3%A9l%C3%A9ments-dune-checklist-dans-le-data-model-et-ensuite)

It has been implemented with Bonita 7.10.3 Community Edition:

It contains an application, a process with 2 forms and a BDM.

Through the application the user can create new check-lists and list existing ones.
From existing check-lists the user can mark items as done. Once a check list is completed it disappears from the page (while still available in database).

Of course this application is really simple, but it might provide a good starting point for a real life implementation.
