
# 🎓 SmartEdu - 智能教育平台后端系统

SmartEdu 是一个基于 Spring Boot 构建的智能教育平台后端系统，集成在线课程管理、考试系统、成绩分析、AI 教师、视频管理、人脸认证等功能，适用于高校课程教学与在线考试场景。

---

## 📌 项目简介

SmartEdu 是一个完整的教学管理 + 在线考试 + 智能分析系统，主要面向：

- 👨‍🏫 教师：课程管理、试卷管理、考试发布、成绩分析
- 👨‍🎓 学生：课程学习、在线考试、成绩查询
- 🛠 管理员：用户管理、系统配置
- 🤖 AI 教师：智能问答（集成大模型接口）
- 📊 数据分析：成绩分析与导出
- 🎥 在线教学：视频与录屏管理
- 👁 人脸认证：考试身份校验

---

## 🚀 技术栈

### 后端框架
- Spring Boot
- MyBatis-Plus
- Maven

### 安全认证
- JWT 登录认证
- 自定义拦截器（JwtInterceptor）
- Token 黑名单机制

### 数据库
- MySQL

### AI & 第三方服务
- 星火大模型接口
- 百度人脸识别
- 阿里云 OSS 文件存储
- Agora 实时音视频

---

## 📂 项目结构

```
SmartEdu
├── db/                         # 数据库脚本
│   └── edu_system.sql
├── src/main/java/com
│   ├── annotation/             # 自定义注解
│   ├── config/                 # 系统配置类
│   ├── controller/             # 控制层
│   ├── dao/                    # 数据访问层（DAO）
│   ├── dto/                    # 数据传输对象
│   ├── entity/                 # 实体类
│   │   ├── view/               # 视图对象
│   │   └── vo/                 # 返回封装对象
│   ├── interceptor/            # JWT 拦截器
│   ├── service/                # 业务接口
│   │   └── impl/               # 业务实现类
│   ├── utils/                  # 工具类
│   └── SpringbootSchemaApplication.java
```

---

## 🔑 核心功能模块

### 👨‍🏫 教师模块
- 创建课程
- 上传课程资料
- 发布作业
- 组卷与发布考试
- 成绩分析
- 导出考试成绩

### 👨‍🎓 学生模块
- 加入课程
- 在线考试
- 作业提交
- 成绩查询

### 📝 考试系统
- 题库管理（单选、多选、判断、填空）
- 自动组卷
- 考试记录
- 成绩统计分析
- Excel 成绩导出

### 📊 成绩分析
- 成绩统计
- 分数分布分析
- 学生成绩详情
- 数据导出接口

### 🤖 AI 教师
- 接入大模型接口
- 智能答疑
- 教学辅助

### 👁 人脸识别
- 考试身份认证

### 🎥 视频系统
- 课程视频管理
- 屏幕录制视频管理

---

## 🛠 数据库初始化

1️⃣ 创建数据库：

```sql
CREATE DATABASE edu_system CHARACTER SET utf8mb4 COLLATE utf8mb4_general_ci;
```

2️⃣ 执行脚本：

```
db/edu_system.sql
```

---

## ⚙️ 启动方式

### 使用 Maven Wrapper

Linux / Mac：

```bash
./mvnw spring-boot:run
```

Windows：

```bash
mvnw.cmd spring-boot:run
```

或直接运行：

```
SpringbootSchemaApplication.java
```

---

## 🔐 登录认证机制

- 使用 JWT 进行登录认证
- 登录成功返回 token
- 请求头中携带：

```
Authorization: Bearer token
```

- 自定义注解 `@IgnoreAuth` 可跳过认证

---

## 📊 成绩导出功能说明

支持：

- 根据考试 ID 导出学生成绩
- 包含：姓名、成绩、考试时间
- 生成 Excel 文件下载

---

## 🧩 项目亮点

✅ 完整的教学管理系统架构  
✅ 前后端分离设计  
✅ JWT + 黑名单机制  
✅ AI 教师接入  
✅ 人脸识别考试认证  
✅ 成绩分析与导出  
✅ 清晰分层结构（Controller / Service / DAO）

---

## 📜 License

本项目仅用于学习与交流，请勿用于商业用途。

---

# ⭐ 如果对你有帮助，欢迎 Star 支持！
