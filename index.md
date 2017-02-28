# Navigation

[comment]: # ([Introduction](/bnsimulator/page2))

- [Introduction](#introduction)
- [Examples](#examples)
- [Author](/bnsimulator/page2)


# Introduction

The _bnsimulator_ is a simulator software written in Java that allows to simulate and perform experiments on Boolean networks with synchronous, asynchronous and others known in the literature updating scheme.


# Examples

1. Simple search of attractors of a RBN with 20 nodes following a synchronous updating scheme: 
```java
BooleanNetwork<MyBitSet, Boolean> bn = new ClassicRBN(20, 3, 0.79);
SynchronousDynamics<MyBitSet> dynamics= new SynchronousDynamicsImplReverse(bn);		//Xn, ..., X1, X0
SampleGenerator<MyBitSet> generator = new CompleteEnumerationBitSet(bn.getNodesNumber());
AttractorsFinder<MyBitSet> finder = new AttractorsFinder<MyBitSet>(dynamics, generator, MyBitSet.MyBitSetComparator);
List<CyclicAttractor<MyBitSet>> attractors = finder.run();
```
2. bla balskjashfa


# Credits

….