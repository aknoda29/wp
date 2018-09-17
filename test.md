## ER Diagram

### Sample 1

```uml
@startuml
    entity "foo" {
        + foo_id
        --
        name
        ...
    }
    entity "bar" {
        + bar_id
        --
        # foo_id
        name
        ...
    }
    foo ||-ri-o{ bar
@enduml
```

### Sample 2

```uml
@startuml
    entity "hoge" {
        + hoge_id
        --
        # parent_hoge_id
        name
        ...
    }
    hoge ||--o{ hoge
@enduml
```