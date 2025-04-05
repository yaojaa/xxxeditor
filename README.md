# Editor.js 类方法文档

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




# Viewport.js 类方法文档

## 方法列表

### 构造函数
- **`Viewport(editor)`**: 初始化 Viewport 实例，设置渲染器、相机、场景等，并添加各种控制和事件监听。

### 渲染器管理
- **`initPT()`**: 初始化路径追踪器（Pathtracer）。
- **`updatePTBackground()`**: 更新路径追踪器的背景。
- **`updatePTEnvironment()`**: 更新路径追踪器的环境。
- **`updatePTMaterials()`**: 更新路径追踪器的材质。
- **`updatePT()`**: 更新路径追踪器。

### 渲染
- **`render()`**: 渲染场景，包括主场景、辅助场景和视图辅助工具。

### 事件处理
- **`handleClick()`**: 处理点击事件，检测交集并触发信号。
- **`onMouseDown(event)`**: 处理鼠标按下事件。
- **`onMouseUp(event)`**: 处理鼠标释放事件。
- **`onTouchStart(event)`**: 处理触摸开始事件。
- **`onTouchEnd(event)`**: 处理触摸结束事件。
- **`onDoubleClick(event)`**: 处理双击事件，聚焦对象。

### 辅助工具
- **`updateAspectRatio()`**: 更新相机的宽高比。
- **`getMousePosition(dom, x, y)`**: 获取鼠标位置。
- **`updateGridColors(grid1, grid2, colors)`**: 更新网格颜色。

### 信号处理
- **`signals.cameraPositionChanged.add(callback)`**: 处理相机位置改变信号。
- **`signals.editorCleared.add(callback)`**: 处理编辑器清除信号。
- **`signals.transformModeChanged.add(callback)`**: 处理变换模式改变信号。
- **`signals.snapChanged.add(callback)`**: 处理快照改变信号。
- **`signals.spaceChanged.add(callback)`**: 处理空间改变信号。
- **`signals.rendererUpdated.add(callback)`**: 处理渲染器更新信号。
- **`signals.rendererCreated.add(callback)`**: 处理渲染器创建信号。
- **`signals.rendererDetectKTX2Support.add(callback)`**: 处理检测 KTX2 支持信号。
- **`signals.sceneGraphChanged.add(callback)`**: 处理场景图改变信号。
- **`signals.cameraChanged.add(callback)`**: 处理相机改变信号。
- **`signals.objectSelected.add(callback)`**: 处理对象选择信号。
- **`signals.objectFocused.add(callback)`**: 处理对象聚焦信号。
- **`signals.geometryChanged.add(callback)`**: 处理几何体改变信号。
- **`signals.objectChanged.add(callback)`**: 处理对象改变信号。
- **`signals.objectRemoved.add(callback)`**: 处理对象移除信号。
- **`signals.materialChanged.add(callback)`**: 处理材质改变信号。
- **`signals.sceneBackgroundChanged.add(callback)`**: 处理场景背景改变信号。
- **`signals.sceneEnvironmentChanged.add(callback)`**: 处理场景环境改变信号。
- **`signals.sceneFogChanged.add(callback)`**: 处理场景雾改变信号。
- **`signals.sceneFogSettingsChanged.add(callback)`**: 处理场景雾设置改变信号。
- **`signals.viewportCameraChanged.add(callback)`**: 处理视口相机改变信号。
- **`signals.viewportShadingChanged.add(callback)`**: 处理视口着色模式改变信号。
- **`signals.windowResize.add(callback)`**: 处理窗口大小改变信号。
- **`signals.showHelpersChanged.add(callback)`**: 处理显示辅助工具改变信号。
- **`signals.cameraResetted.add(callback)`**: 处理相机重置信号。

### 动画
- **`animate()`**: 动画循环，更新混合器、视图辅助工具和路径追踪器。
