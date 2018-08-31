---
title: Scala
category: Others
---

## Java Converstions

```Scala
import scala.collection.JavaConverters._

javaList.asScala
```

## For Comprehension

```Scala
val froidConfig = for {
    host <- scala.util.Properties.envOrNone("host")
    port <- scala.util.Properties.envOrNone("port").flatMap(p => Try(p.toInt).toOption)
  } yield {
    Params(
      host,
      port
    )
  }
```

## Postfix Ops

```Scala
import language.postfixOps
```