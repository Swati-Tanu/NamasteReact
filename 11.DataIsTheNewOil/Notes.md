Higher order component

Implementing Promoted label display use HOC

HOC is a Pure Function as we are just adding/enhancing some extra feature. We are not chnaging anything in the functionality of the component that we are taking as argument.


accordion : where we can expand and collapse 

uplifting the state
controlled and uncontrolled component

React has one way data stream. Grand Parent -> Parent -> Child -> Grand Child
If we can to pass a data Grand Parent to Grand Child, I have to pass through Parent and Child even if that data has nothing do with them. This comcept is called Props Drilling.

React Context is one of the way that solves the issue of Props Drilling.

Some data that can be needed all across the app
Logged in user name
dark/while theme

Using React context can help not use external state management library like Redux in small or medium sized apps.


