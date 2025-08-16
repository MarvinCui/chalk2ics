# 希悦课表日程转换器

将希悦教务系统导出的Excel课表文件转换为ICS日历文件，支持导入到各种日历应用中。

## 功能特点

- 📅 支持Excel (.xlsx) 课表文件解析
- 🕐 自动识别时间段和星期安排
- 📱 响应式设计，支持移动端和桌面端
- 🌏 默认使用北京时间 (Asia/Shanghai)
- 📋 支持自定义总周数和特殊行处理
- 💾 生成标准ICS格式文件，兼容主流日历应用

## GitHub Pages 部署

### 方法一：直接部署

1. Fork 或下载此项目到你的 GitHub 仓库
2. 在仓库设置中启用 GitHub Pages
3. 选择 `main` 分支作为源
4. 访问 `https://你的用户名.github.io/仓库名` 即可使用

### 方法二：自定义域名

1. 在仓库根目录创建 `CNAME` 文件
2. 在文件中写入你的自定义域名（如：`schedule.example.com`）
3. 在域名DNS设置中添加CNAME记录指向 `你的用户名.github.io`

## 本地开发

由于使用了本地JavaScript库，可以直接在浏览器中打开 `index.html` 文件使用，无需启动服务器。

```bash
# 克隆项目
git clone <repository-url>
cd <repository-name>

# 直接在浏览器中打开
open index.html
```

## 使用说明

1. **准备Excel文件**：从希悦教务系统导出课表Excel文件
2. **设置第一周周一日期**：确保日期准确，影响整个学期的课程安排
3. **配置参数**：
   - 总周数：用于没有标注具体周数的课程
   - 入校考勤：是否包含考勤时间段
   - 中午时段：是否包含午休时间
4. **生成并下载**：点击生成按钮，然后下载ICS文件
5. **导入日历**：将ICS文件导入到你的日历应用中

## 支持的日历应用

- 📱 Apple 日历 (iOS/macOS)
- 📧 Google Calendar
- 💼 Microsoft Outlook
- 📅 其他支持ICS格式的日历应用

## 技术栈

- **前端**：原生HTML/CSS/JavaScript
- **Excel解析**：SheetJS (xlsx.js)
- **时间处理**：Luxon.js
- **部署**：GitHub Pages 静态托管

## 文件结构

```
.
├── index.html          # 主页面（GitHub Pages入口）
├── style.css           # 样式文件
├── xlsx.full.min.js    # Excel解析库
├── luxon.min.js        # 时间处理库
├── .gitignore          # Git忽略文件
└── README.md           # 项目说明
```

## 注意事项

- 建议在选课完成后的学期中期下载Excel文件，确保数据完整性
- 如果某天某节课没有安排，导出的Excel中不会包含该时段
- 生成的ICS文件使用北京时间，如需其他时区请修改代码
- 支持课程名称自动简化，去除教师和教室信息

## 许可证

MIT License

## 贡献

欢迎提交Issue和Pull Request来改进这个项目！