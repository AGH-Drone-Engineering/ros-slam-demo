# SLAM Demo

## Usage

1. Install requirements
    - Docker
    - a VNC client

2. Place a video file inside [video/](/video/)

3. Update video filename inside [camera/video.launch](/camera/video.launch)

4. Run with docker compose:

    ```bash
    docker compose up --build
    ```

5. Connect with VNC to `localhost:5900`

6. From bottom left menu select System Tools -> LXTerminal

7. Run `rviz`

8. Use Add button to visualize the pointcloud and TF transform

9. Change reference frame in top left to `map_view`
