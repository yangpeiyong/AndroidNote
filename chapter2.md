# Fragment Transactions & Activity State Loss

无讼阅读5.0上线之后，后台统计最多的异常如下：
```
java.lang.IllegalStateException: Can not perform this action after onSaveInstanceState
	at android.support.v4.app.FragmentManagerImpl.checkStateLoss(FragmentManagerImpl.java:1493)
	at android.support.v4.app.FragmentManagerImpl.enqueueAction(FragmentManagerImpl.java:1511)
	at android.support.v4.app.BackStackRecord.commitInternal(BackStackRecord.java:634)
	at android.support.v4.app.BackStackRecord.commit(BackStackRecord.java:613)
```

本文将介绍这种异常出现的原因，以及如何避免出现这样的一场。