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
  status
  release_date
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
object video_gameworker {
  video_id<pk>
  url
  worker_game_id<fk>
  video_telop<fk>
}
object video_movieworker {
  video_id<pk>
  url
  worker_movie_id<fk>
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
video_gameworker *-- video : 1:N
video_movieworker *-- video : 1:N
worker_game *-- video_gameworker : 1:N
worker_movie *-- video_movieworker : 1:N
video_tag *-- video : 1:N
@enduml
```