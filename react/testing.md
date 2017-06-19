# Testing

## Jest

snapshot testing

parallel runs

mockups

built on Jasmine

built in test-coverage reporting (Instabnul)

Instead of using `react-test-renderer` it is recommended to use Enzyme as it allows shallow rendering of components and then only relevant tests fail rather than the parent tests. Enzyme is just a wrapper around react-test-renderer.

```import {shallow} from enzyme;

    const component = shallow(<MyComponent />)
    expect(component).toMatchSnapshot();
    
```

events can be triggered using simulate for e.g. 

```
component.find('input').simulate('change', { target: { value: searchText}})
```