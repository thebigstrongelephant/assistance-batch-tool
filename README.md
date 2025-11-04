# 助力金批量下发工具

一个完整的助力金批量下发管理系统，支持多种下发方式、运营活动配置和实时监控。

## 🎯 功能特点

### 📤 批量下发
- **多种下发方式**：按地区下发、Excel导入村庄ID
- **地区选择**：支持省/市/镇/村四级筛选，包含"全部"选项
- **助力金配置**：统一金额设置、有效期选择、自定义说明
- **模板消息**：自定义消息标题和内容，支持变量替换
- **实时预览**：村庄列表预览、总金额计算

### ⚙️ 运营活动配置
- **村委首次获取奖励**：自动奖励机制
- **村庄活跃度奖励**：基于申请数量的奖励倍数
- **节假日特殊活动**：时间段和特殊金额配置

### 📊 助力金波动监控
- **趋势图表**：下发趋势、地区分布
- **异常监控**：异常增长、兑换率下降、大额集中下发

### 📋 审核管理
- **任务审核**：待审核任务列表、一键通过/驳回
- **统计数据**：审核数量、时长、通过率
- **历史记录**：完整的审核轨迹

## 🚀 在线预览

访问地址：[https://your-username.github.io/assistance-batch-tool/](https://your-username.github.io/assistance-batch-tool/)

## 📱 界面展示

- **PC端优化**：响应式设计，适配不同屏幕尺寸
- **标签页导航**：清晰的功能模块划分
- **实时交互**：拖拽上传、实时预览、智能验证
- **用户体验**：加载状态、通知提示、错误处理

## 🛠️ 技术栈

- **前端**：HTML5 + CSS3 + JavaScript (ES6+)
- **样式**：自定义CSS，现代化UI设计
- **交互**：原生JavaScript，无依赖框架
- **部署**：GitHub Pages

## 📦 本地运行

1. 克隆仓库
```bash
git clone https://github.com/your-username/assistance-batch-tool.git
cd assistance-batch-tool
```

2. 直接打开HTML文件
```bash
# 使用浏览器打开
open 批量下发工具.html
# 或者使用本地服务器
python -m http.server 8000
```

## 🔧 配置说明

### 地区数据配置
在JavaScript中修改 `cities` 和相关数据结构来配置实际的地区数据。

### 模板消息配置
支持以下变量：
- `{amount}` - 助力金金额
- `{village_name}` - 村庄名称
- `{expire_date}` - 到期日期

### Excel模板格式
- `village_id` - 村庄ID（必填）
- `village_name` - 村庄名称（可选）
- `amount` - 助力金额（可选）

## 📄 许可证

MIT License

## 🤝 贡献

欢迎提交 Issue 和 Pull Request！

## 📞 联系方式

如有问题，请通过 GitHub Issues 联系。