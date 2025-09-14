Using state manager libraries are not mandatory

In large scale app state manager libraries helps to handle data, manage state, app becomes easier to debug, etc.

State Manager Library:
Redux
Zustand

Redux libraries:
React-Redux
Redux Toolkit

Redux store is a big js object that is kept at a global central place. This store can be access from any component of the app.

Since this store has most of the major data it can become very big, clumsy and unmanagable. so we can divide it into small portion called slices. Eg. cart slice, user slice, theme slice, etc.

RTK Architecture
Redux Store --> divided into small slices
1. Make changes to the store
Eg, If I add a product to my cart, how does the data go to my cart slice (WRITE Operation). We cannot modify the slice directly. Following are the steps to follow:

When we click on the Add button --> it "dispatches" as "action" --> which calls a function called "reducer" --> this reducer function modifies/updates the slice of the Redux store.

2. Read from the store
Eg, Once product is added how is data displayed on the cart, or the number of product is increase (READ Operation). Following are the steps to follow: 

We use "selector" to read the data from the slice of our store --> this "selector" will display the data (i.e., increase the no./add the data) --> this phenomena is called "Subscribing to the store".

Eg, Header component (where cart exists) is subscribed to the store using the selector so the header component will update automatically if any changes are made in the store.