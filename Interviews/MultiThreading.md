#### [1] lock and Value Type

We cannot use a Value Type with the ```lock``` keyword because a value type does not contain a Sync Block Index.

```cs 
lock(<reference type>)
```
