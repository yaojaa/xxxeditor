# Editor 类方法文档

## 方法列表

### 构造函数
- **`Editor()`**: 初始化 Editor 实例，设置默认相机和其他属性。

### 场景管理
- **`setScene(scene)`**: 设置当前场景。
- **`addObject(object, parent, index)`**: 向场景中添加对象。
- **`moveObject(object, parent, before)`**: 移动对象到指定位置。
- **`nameObject(object, name)`**: 重命名对象。
- **`removeObject(object)`**: 从场景中移除对象。
- **`clear()`**: 清空编辑器状态，恢复默认设置。

### 几何体管理
- **`addGeometry(geometry)`**: 添加几何体。
- **`setGeometryName(geometry, name)`**: 设置几何体名称。

### 材质管理
- **`addMaterial(material)`**: 添加材质。
- **`addMaterialToRefCounter(material)`**: 增加材质引用计数。
- **`removeMaterial(material)`**: 移除材质。
- **`removeMaterialFromRefCounter(material)`**: 减少材质引用计数。
- **`getMaterialById(id)`**: 根据 ID 获取材质。
- **`setMaterialName(material, name)`**: 设置材质名称。

### 纹理管理
- **`addTexture(texture)`**: 添加纹理。

### 相机管理
- **`addCamera(camera)`**: 添加相机。
- **`removeCamera(camera)`**: 移除相机。

### 辅助对象管理
- **`addHelper(object, helper)`**: 添加辅助对象。
- **`removeHelper(object)`**: 移除辅助对象。

### 脚本管理
- **`addScript(object, script)`**: 添加脚本。
- **`removeScript(object, script)`**: 移除脚本。

### 数据绑定管理
- **`addData(object, data)`**: 添加数据绑定。
- **`removeData(object, data)`**: 移除数据绑定。

### 对象操作
- **`getObjectMaterial(object, slot)`**: 获取对象的材质。
- **`setObjectMaterial(object, slot, newMaterial)`**: 设置对象的材质。
- **`select(object)`**: 选择对象。
- **`selectById(id)`**: 根据 ID 选择对象。
- **`selectByUuid(uuid)`**: 根据 UUID 选择对象。
- **`deselect()`**: 取消选择。
- **`focus(object)`**: 聚焦对象。
- **`focusById(id)`**: 根据 ID 聚焦对象。

### 视口设置
- **`setViewportCamera(uuid)`**: 设置视口相机。
- **`setViewportShading(value)`**: 设置视口着色模式。

### JSON 操作
- **`fromJSON(json)`**: 从 JSON 数据恢复场景。
- **`toJSON()`**: 将当前场景转换为 JSON 数据。
- **`sceneToJSON()`**: 将场景转换为 JSON 数据，移除 CSS3DObject。

### 工具方法
- **`objectByUuid(uuid)`**: 根据 UUID 获取对象。
- **`execute(cmd, optionalName)`**: 执行命令。
- **`undo()`**: 撤销上一步操作。
- **`redo()`**: 重做上一步操作。
