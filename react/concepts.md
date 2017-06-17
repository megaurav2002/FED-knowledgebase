# Concepts

## One way data flow -

Parent can pass down data to child but vice versa is not allowed. Child can only accept data from Parent and is called one way data flow i.e. Props are immutable. Its a really good thing because it makes troubleshooting a lot simpler. for e.g if you have a problem component, you can easily rule out the child as a source because child does not push the data up to the parent.