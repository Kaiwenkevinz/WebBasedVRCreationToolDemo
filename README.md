# Web-Based-VR-Creation-Tool

## Demo
![demo](https://github.com/Kaiwenkevinz/Web-Based-VR-Creation-Tool-Demo/blob/main/imgs/video_demo.gif?raw=true)
## 如何使用 Yjs 获得实时数据？
监听 Yjs Shared Types
![yjs](https://github.com/Kaiwenkevinz/Web-Based-VR-Creation-Tool-Demo/blob/main/imgs/yjs_overview.png?raw=true)

## 使用树形结构前，如何获取最新值并渲染？
组件 A 监听字符串 A -> 用户更新字符串 -> 回调中获取字符串 A 最新值 -> 调用相应的 setState  
组件 B 监听字符串 B -> 用户更新字符串 -> 回调中获取字符串 B 最新值 -> 调用相应的 setState  
组件 C 监听字符串 C -> 用户更新字符串 -> 回调中获取字符串 C 最新值 -> 调用相应的 setState  
![before_tree](https://github.com/Kaiwenkevinz/Web-Based-VR-Creation-Tool-Demo/blob/main/imgs/before_tree.png?raw=true)

## 使用树形结构后，如何获取最新值并渲染？
所有组件监听根节点 -> 用户更新字符串 -> 监听回调得到树，树中包含了最新值 -> 调用 setState，传入 JSON 化的树
![after_tree](https://github.com/Kaiwenkevinz/Web-Based-VR-Creation-Tool-Demo/blob/main/imgs/after_tree.png?raw=true)