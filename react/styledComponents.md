# Styled Components

Bring all the styling into the components. Allows you to write CSS in JavaScript. Styling can be applied based on props e.g. 

```
const Button = styled.button`
  border-radius: 3px;
  padding: 0.25em 1em;
  margin: 0 1em;
  background: transparent;
  color: palevioletred;
  border: 2px solid palevioletred;

  ${props => props.primary && css`
    background: palevioletred;
    color: white;
  `}
`
```

### Links

https://www.styled-components.com/

https://www.styled-components.com/docs/basics#motivation