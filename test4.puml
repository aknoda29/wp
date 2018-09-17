```uml
@startuml
' -- Theme --------------------
object theme {
  theme_id<pk>
  theme_info{...}
  game_id<fk>
}
' -- Game --------------------
object game {
  game_id<pk>
  game_info{...}
}
' -- Video -------------------
object video {
  video_id<pk>
  video_info{...}
  worker_game_id<fk>
  worker_movie_id<fk>
}
object video_telop {
  video_id<pk>
  telop_id<pk>
  telop_start_time
  telop_end_time
  telop_info{...}
}
object video_tag {
  video_id<pk>
  tag<pk>
}
' -- Worker -------------------
object worker_game {
   worker_game_id<pk>
   name
}
object worker_movie {
   worker_movie_id<pk>
   name
}
' -- Diagram -----------------
game *-- video : 1:N
video *-- video_telop : 1:N
video *-- video_tag : 1:N
game *-- theme : 1:N
theme *-- video : 1:N
worker_game *-- video : 1:N
worker_movie *-- video : 1:N
@enduml
```
