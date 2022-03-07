

https://www.youtube.com/watch?v=bqu6BquVi2M&list=PLpGHT1n4-mAsxuRxVPv7kj4-dQYoC3VVu&index=1

## Lecture 1:
- 

## Lecture 2:
- Library of commonly used symbols that can be added to Apps: (developer.apple.com/sf-symbols)
- 

## Lecture 3:
Model-Video-ViewModel:
-	A "code organizing" architectural design paradigm.
-	Must be adhered to for SwiftUI to work
-	It is different from MVC (Model View Controller) that UIKit (old-style iOS) uses
-	Separates `The View` (the user interface) from `The Model`(logic of the application)

The Model:
- UI Independent
- Data and Logic
- The single source of "Truth" about the app

The View:
- Reflects the Model
- Stateless
- Declared (View is determined by what is in `body` variable)
- Reactive (reacts efficiently to changes in the Model due to the fact that the View is immutable and has to be rebuilt every time it changes)

The ViewModel:
- Binds View to Model as an intermediary
- Interpreter between Model and View (Model is an SQL database, or has HTTP requests, etc.). Works to make sure that the functions in the Model called by the View are "exactly what the View needs"
- Gatekeeper for the Model, making sure that access to the Model is "well behaved"
- Tracks changes in the Model, the publishing that "something has changed" to the entire world. This is because the ViewModel does not want to have any connections to any of the Views that are using it to access the Model.
- "Processes user intent" sent from the View as the user interacts with it. It then translates those intentions into specific modifications for the Model

- The View must always get data from the Model by asking it through the ViewModel
		- The ViewModel never stores the data for the Model inside of itself
		- Views "subscribe" to what the ViewModel is publishing when it says something has changed in the model

- We **NEVER** have a pointer or any other data structure in a ViewModel that knows anything about a View struct.