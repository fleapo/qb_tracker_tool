# [qb_tracker_tool](https://github.com/fleapo/qb_tracker_tool)
批量管理qBittorrent tracker的[油猴脚本](https://greasyfork.org/zh-CN/scripts/539174-xyg-qbittorrent-tracker%E6%89%B9%E9%87%8F%E6%93%8D%E4%BD%9C%E8%84%9A%E6%9C%AC)

## 使用方法

### 安装
1. 安装油猴插件, [Tampermonkey](https://www.tampermonkey.net/)
2. 安装脚本, [qb_tracker_tool](https://greasyfork.org/zh-CN/scripts/539174-xyg-qbittorrent-tracker%E6%89%B9%E9%87%8F%E6%93%8D%E4%BD%9C%E8%84%9A%E6%9C%AC)


### 使用前，油猴设置，让脚本在你特定的QB Web UI地址上生效
1. 在油猴插件中，找到qb_tracker_tool脚本
2. 点击qb_tracker_tool脚本对应的编辑按钮
3. 进入编辑页面后，点击左上方的"设置"选项卡
4. "包括/排除"设置区域，在"用户包括"(精准匹配url)或"用户匹配"(支持通配符匹配特定样式的url)中，添加自己的QB Web UI访问地址
5. 点击页面最下方的"保存"


### 使用，以"替换"为例
1. 选择"操作模式"单选框中的"替换"
2. 选择使用分类筛选或使用标签筛选
3. 在标签输入框中输入要筛选的标签名称
4. 点击"预览"按钮查看符合条件的种子（可选但推荐）
5. 在"旧 Tracker"输入框中输入要替换的tracker地址
6. 在"新 Tracker"输入框中输入要替换为的tracker地址，每行一个
7. 点击"替换"按钮执行操作

## 版本 1.0.0 新功能

### 1. 标签筛选功能
- 新增按标签筛选种子的功能
- 在界面上方添加了单选框，可以选择"按分类筛选"或"按标签筛选"

### 2. 多行Tracker支持
- 在"替换"和"添加"操作中，新Tracker输入框改为多行文本框
- 支持一次性输入多个tracker地址（每行一个）
- 在替换操作中，会先替换第一个tracker，然后添加其余的tracker
- 在添加操作中，会一次性添加所有输入的tracker

### 3. 预览功能
- 新增预览按钮，可以在执行操作前查看符合条件的种子的tracker列表
- 只显示有效的tracker URL，过滤掉已被禁用的tracker
- 自动去重，只显示唯一的tracker地址