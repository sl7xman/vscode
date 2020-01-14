# ubuntu安装vscode与编译c++

## 编译步骤
    
    1、安装c++扩展
    2、创建项目目录
      mkdir project/hello
      cd hello
    3、在该项目主目录下执行命令
      code .
      即：vscode默认以当前目录为项目目录
    4、在vscode中创建新源码文件 main.cpp 编写简单的hello 代码
    5、在“终端”菜单选择“生成默认任务”，在弹出菜单选择“g++ build active file",会生成task.json文件，内容为
    
```
    {
// 有关 tasks.json 格式的文档，请参见
    // https://go.microsoft.com/fwlink/?LinkId=733558
    "version": "2.0.0",
    "tasks": [
        {
            "type": "shell",
            "label": "g++ build active file",
            "command": "/usr/bin/g++",
            "args": [
                "-g",
                "${file}",
                "-o",
                "${fileDirname}/${fileBasenameNoExtension}"
            ],
            "options": {
                "cwd": "/usr/bin"
            },
            "problemMatcher": [
                "$gcc"
            ],
            "group": {
                "kind": "build",
                "isDefault": true
            }
        }
    ]
}
    ```
