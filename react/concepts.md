# Concepts

## One way data flow

Parent can pass down data to child but vice versa is not allowed. Child can only accept data from Parent and is called one way data flow i.e. Props are immutable. Its a really good thing because it makes troubleshooting a lot simpler. for e.g if you have a problem component, you can easily rule out the child as a source because child does not push the data up to the parent.

## Lifecycle Methods

Things happen in the following order

constructor >> componentWillMount >> render >> componentDidMount >> componentWillUnmount

componentWillReceiveProps

shouldComponentUpdate


### componentWillMount

Called right before react renders the component to the DOM. Not used that much. It does get called on server in case of server side rendering.


### componentDidMount

Called right after the component has been rendered to the DOM for the very first time. It does get used more compared to the other lifecycle methods. Window variable is availble here. Can be used for AJAX calls etc or if you want to integrate with another library for e.g. rendering a d3 library component in here.

### componentWillUnmount

Right before the component is removed. All the clean up stuff should happen here i.e. detaching from D3, removing event listeners etc..


## Links

https://facebook.github.io/react/docs/react-component.html