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

Notice, how with concatAll the resultant stream is longer than the individual streams. This is an approach to resolve race conditions. You don't want to use concatAll on an infinite stream as concatAll needs to finish one before moving on to the other ones.

### Take Until

Instead of calling removeeventlistener, we combine two streams so that you stop listening to stream 1 when stream 2 starts emitting

```

    { // start collection
        1......2...........3
    }
    { // stop collection
        ............4
    }


so you get


    {
        1.......2
    }

```