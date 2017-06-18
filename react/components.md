# React Components

## Functional/Stateless components

```
const title = () => <div>this is title</div>
```

## Stateful component

```
Class title extends Components {

    constructor(props) {
        super(props);
        this.state({"title": ""})
    }

    render() {
        return (
            <div>this.state.title</div>
        )
    }

}
```

### Event param

event param passed on onChange etc is not actually the DOM event, it's custom react event which is pretty much same as the DOM event. 
