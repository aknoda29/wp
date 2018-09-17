```uml
@startuml
' -- Game --------------------
object game {
  game_id
  game_info{...}
}
' -- Video -------------------
object video {
  video_id<pk>
  video_info{...}
  owner_id<fk>
}
object video_chapter {
  video_id<pk>
  chapter_id<pk>
  chapter_info{...}
}
object video_tag {
  video_id<pk>
  tag<pk>
}
object pickup_video {
  pickup_id<pk>
  video_id
  pickup_info{...}
}
' -- Diagram -----------------
game *- video : 1:N
video *-- video_chapter : 1:N
video *-- video_tag : 1:N
video *. pickup_video : M:N
@enduml
```
