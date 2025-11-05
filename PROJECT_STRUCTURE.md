# L2J Mobius Classic 2.6 HighFive 项目结构

## 目录说明

### 根目录文件
- `build.xml` - Ant 构建文件，用于编译和打包项目
- `.classpath` - Eclipse 项目类路径配置
- `.project` - Eclipse 项目配置文件
- `.gitignore` - Git 忽略文件配置

### 主要目录
- `java/` - Java 源代码目录，包含所有服务器端代码
- `bin/` - 编译后的类文件目录
- `dist/` - 分发目录，包含服务器运行所需的所有文件
  - `game/` - 游戏服务器相关文件
  - `login/` - 登录服务器相关文件
  - `libs/` - 依赖库文件
  - `MySql/` - MySQL 数据库相关文件
- `SQL/` - 数据库脚本文件
- `.vscode/` - VS Code 编辑器配置
- `.settings/` - Eclipse 项目设置

### 游戏服务器核心功能
- AI 系统 (`bin/ai/`)
- 自定义功能 (`bin/custom/`)
- 游戏事件 (`bin/events/`)
- 副本实例 (`bin/instances/`)
- 处理器 (`bin/handlers/`)
- 任务系统 (`bin/quests/`)

## 构建和运行

1. 使用 Ant 构建项目：
   ```
   ant jar
   ```

2. 启动游戏服务器：
   ```
   cd dist/game
   ./GameServer.sh (Linux/Mac)
   GameServer.bat (Windows)
   ```

3. 启动登录服务器：
   ```
   cd dist/login
   ./LoginServer.sh (Linux/Mac)
   LoginServer.bat (Windows)
   ```

## 开发环境要求

- Java 25
- Apache Ant 1.8.2+
- MySQL 5.7+
- Eclipse IDE (推荐) 或其他 Java IDE