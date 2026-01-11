# 题目刷题工具

这是一个功能完整的题目练习系统，包含客观题和主观题两种题型的录入与练习功能。项目分为两个主要模块，分别支持不同类型的题目处理，帮助用户进行高效的学习和练习。

## 项目结构

项目分为两个主要部分：

- **[Objective-Question](./src/Objective-Question)**：客观题刷题器
  - [obj-insert.cpp](./src/Objective-Question/obj-insert.cpp)：客观题录入程序
  - [obj-quiz.cpp](./src/Objective-Question/obj-quiz.cpp)：客观题测验程序

- **[Subjective-Question](./src/Subjective-Question)：主观题刷题器**
  - [sub-insert.cpp](./src/Subjective-Question/sub-insert.cpp)：主观题录入程序
  - [sub-quiz.cpp](./src/Subjective-Question/sub-quiz.cpp)：主观题练习程序

## 功能特点

### 客观题刷题器
- 支持三种题型：判断题、单选题、多选题
- 题目录入功能，可自定义选项数量（2-9个）
- 测验功能，支持顺序答题和随机答题两种模式
- 自动统计正确率，并记录错题到文件中

### 主观题刷题器
- 支持主观题及参考答案的录入
- 练习功能，支持顺序答题和随机答题两种模式
- 答题后可查看参考答案进行对比
- 自动记录用户答案和参考答案到文件中

## 编译与使用

### 客观题刷题器
```bash
cd src/Objective-Question
g++ obj-insert.cpp -o obj-insert
g++ obj-quiz.cpp -o obj-quiz
```

### 主观题刷题器
```bash
cd src/Subjective-Question
g++ sub-insert.cpp -o sub-insert
g++ sub-quiz.cpp -o sub-quiz
```

详细使用方法请参见各模块下的README.md文件：
- [Objective-Question/README.md](./src/Objective-Question/README.md)
- [Subjective-Question/README.md](./src/Subjective-Question/README.md)

## 文件说明

- `obj-answers.txt` / `sub-answer.txt`：自动记录错题或练习答案
- `.txt` 文件：题库文件，存储题目数据
- 各模块的README.md：详细使用说明

## 技术特点

- **采用 GB2312 编码**
- 纯C++实现，无需额外依赖
- 文件格式简单，易于维护
- 支持Windows/Linux/Mac平台
- 界面简洁，操作方便