# React Meetup Feb 15 2018
### React Router

Intro to React Router

Eve Porcello
eve@@moonhighway.com
@eveporcello

Writes Books about Software

Quick Dive into React Router

Library, not a framework

Ryan Florence & Michael Jackson

One of the most popular tools is React Router in React Ecosystem

First Commit May 9, 2014

Now at Version 4 of React Router

Whats New?

Two Pieces:
React-router-dom
React-router-native

Old way Nested Routes in the Router

HashRouter for Static Websites examples Netlify, Github Pages, testing

BrowserRouter for Dynamic Sites with a server that handles dynamic requests

Both work the same way
Both use similar syntax

GitHub Link:
www.github.com/eveporcello/react-router-houston

Free book link to Learning React in the repo

Setup Routes with HashRouter 

`<HashRouter>`

`	<Switch>`

`		<Route exact path=“/” component={ComponentName} />`

`		<Route component={ComponentName} /> ## Fallback Route`

`	</Switch>`

`</HashRouter>`

exact helps us define the parent route of the other routes
Use exact when a parent router has children routes


How does react know to display the routes if we don’t supply a route . As long as we supply the root route it will display that route.

You can supply  { location } as a prop in a component to access location in the component.

There are special setups for using React-Router with Redux

You don’t have to use react-router to route. There are other methods to use.

PageTemplate will render a template and pass in {children}  to render the children in that component and render it inside the PageTemplate component. This is how to handle nested navigation with react-router

`const PageTemplate = ({ children }) => `

`	<div className="page">`

`		<MainMenu />`

`		{ children }`

`	</div>`


`export const Vans = () => `

`	<PageTemplate>`

`		## This will setup the sub routes for Vans`

`		<Router path="/star-wars" component={StarWars} />`

`		<Router path="/horse" component={Horse} />`

`		<Router path="/snake-and-wolf" component={SnakeAndWolf} />`

`	</PageTemplate>`


