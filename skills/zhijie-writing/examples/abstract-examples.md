# Abstract Examples

These examples are synthetic and are not derived from or copied from the source corpus.

## Mechanism unit

```text
Claim: A delivery estimate changes when the system batches nearby orders.
Evidence: A logged sample shows longer waits at a stated batch size and time window.
Explanation: Batching reduces travel per order but adds queue time.
Inference: The fastest individual trip is not always the fastest system policy.
Consequence: A viewer can predict when batching helps and when it hurts.
```

## Bounded analogy

```text
Model: Treat the queue as a line with a service rate.
Grounding: Work one small numerical example.
Boundary: Real demand is bursty, workers differ, and the service rate changes.
Return: Use the model to explain the observed delay, without claiming the system is literally a fixed queue.
```
