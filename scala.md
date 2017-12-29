---
title: Scala
category: Others
---

## Java Converstions

```scala
import scala.collection.JavaConverters._

javaList.asScala
```

## For Comprehension

```scala
val froidConfig = for {
      host <- scala.util.Properties.envOrNone("froidHost")
      port <- scala.util.Properties.envOrNone("froidPort").flatMap(p => Try(p.toInt).toOption)
    } yield {
      FroidParams(
        host,
        port
      )
    }
```

