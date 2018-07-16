## Project: Search and Sample Return

---

**resolution=1024 x 768**

**Graphics quality=Good**

**FPS=18**

 + I populated the `perception_step` function in `perception.py` with color thresholds and visual output of color thresholds and world map output.
 + To decrease the time to explore the area (and find the rock samples), I doubled the `throttle_set` and increased `max_vel` to 3. However, to prevent rollovers around the walls, I also increased the `stop_forward` threshold to 300 in order to stop earlier when there is not enough navigable space in front of rover.
 + To increase map fidelity, I do not update the world map when rover's pitch or roll exceed 1 degree from zero. 
 + To reduce re-visiting the same places, when computing the steering angle by averaging navigable angles, I use higher weights for the new pixels and lower weight for pixels that existed in the map. So converting the unweighted averaging to a weighted averaging of angles to compute the steering.


