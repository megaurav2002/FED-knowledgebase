# Observables

Thinking of events as an array of items. By using an iterator on an array, you can ask for next item till it returns done.

Similarly, with observables on events you can have three functions that get called on an event e.g. mousemove event - onNext, onError, onCompleted. (PUSH) 

iterators are pull whereas observables are push

## Strategies to Flatten

```{
{
    1...........2......3...4
}
{
    ....5.......................6
}


}```

### Concat All

This finishes the first observables and then moves on the next one

so, you get the below even though 5 arrived before 2

```
{
 1...........2......3...4..5.......................6
}```

Notice, how with concatAll the resultant stream is longer than the individual streams. This is an approach to resolve race conditions.