# React Import--with curly bracket vs without
There are two ways to import componets or functions in React--with curly bracket or without. The diffence of the two depends on how the exports are defined in the source.

## 1) Single Default Item

When the source module exports a single default item, we can import it without the curly bracket

```
import FunComponent from "../component/FunComponent"
```

## 2) Mutiple items

When there are multiple export items (or functions), use the curly brackets to specify each import.
```
import { Lol, Wtf, Omg } from "../components/Acronym"
```