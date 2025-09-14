## Developer Testing

1. Manual Testing
2. Writing Test Cases to test component

Types of Testing using Test Cases

- Unit Testing: Testing one unit/component/endpoint in isolation.
- Integration Testing: Testing the intraction between 2 or more unit/component/endpoint.
- End-to-end Testing (e2e testing): Testing complete platform, right from landing page to every single features, in many different flow.

We will use React Testing Library -- it uses jest behind the scenes.

### Setup

- Install React Testing Library
- Install Jest
- Install Babel configuration (as we are using parcel to create app and parcel uses babel behind the scene)
- Create conifigure Babel file
- Create configure Parcel file to disable default Babel transpilation (so that it does not conlict with Jest's Babel config).
- Jest configuration - npx jest --init --> will ask some questions and create jest configure file.
- Install jsdom library
- Install @babel/preset-react to make JSX work in test case
- Include @babel/preset-react inside babel config
- Install @testing-library/jest-dom

When test cases runs it does not run on browser or server, it needs an testing environment, here we are using jsdom, it can be node also.

\_\_ (2 underscores) are called Dunder method.

test.only - to run only one test case
test.skip - to skip any test case

"it" keyword can also be used in place of "test"

If we test a component that has anything other than react code, e.g., Redux, Link (react router dom), fetch. The test will fail as it does not understand it. To solve this we have to provide the store to the Compoent we are testing. E.g., Header.
