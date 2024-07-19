# map_height_fitter

This library fits the given point with the ground of the point cloud map. 将给定的点与点云图匹配
The map loading operation is switched by the parameter `enable_partial_load` of the node specified by `map_loader_name`.
The node using this library must use multi thread executor. 这个库必须用多线程

## Parameters

{{ json_to_markdown("map/map_height_fitter/schema/map_height_fitter.schema.json") }}

## Topic subscription

| Topic Name       | Description                                                                                  |
| ---------------- | -------------------------------------------------------------------------------------------- |
| ~/pointcloud_map | The topic containing the whole pointcloud map (only used when `enable_partial_load = false`) |

## Service client

| Service Name       | Description                         |
| ------------------ | ----------------------------------- |
| ~/partial_map_load | The service to load the partial map |
