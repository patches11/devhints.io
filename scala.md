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
    host <- scala.util.Properties.envOrNone("froidHost")
    port <- scala.util.Properties.envOrNone("froidPort").flatMap(p => Try(p.toInt).toOption)
  } yield {
    FroidParams(
      host,
      port
    )
  }
```

