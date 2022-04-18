# ScalaMock Classes with Constructors

A class with a constructor where the constructor takes arguments and uses these to setup the instance like

```scala
class EdgeClient(config: Config) {
  val edgeId = config.client.edgeId
}
```

will often result in a null-pointer exception when ScalaMock tries to mock it because ScalaMock just passes `null` as the constructor arguments.

A solution is to make the the members `lazy` since they won't be called (only the mock will).

Alternatively we can create another class extending the first

```scala
class MockableEdgeClient extends EdgeClient(config)
val m = mock[MockableEdgeClient]
```

