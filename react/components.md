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
