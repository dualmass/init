# init

```scala
var state: Any = _

override def receiveRecover: Receive = {
  case SnapshotOffer(metadata, offeredSnapshot) ⇒ state = offeredSnapshot
  case RecoveryCompleted                        ⇒
  case event                                    ⇒ // ...
}
```
