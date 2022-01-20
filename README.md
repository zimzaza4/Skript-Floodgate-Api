# Skript-Floodgate-Form
A simple script

Allows the use of simple Skript to make Forms

**How to install?** 
- After confirming to install all dependent plugins, put this script into plugins/Skript/scripts/ and reload it


**如何安装?**
- 装上Skript, Skript-Reflect, [BEMenuAPI](https://github.com/zimzaza4/Skript-Floodgate-Form/releases/tag/1.0) 插件
- 将该脚本放入该放的文件夹 plugins/Skript/scripts/
- 启动服务器


The script depends on plugins:
- Skript
- Skript-Reflect
- [BEMenuAPI](https://github.com/zimzaza4/Skript-Floodgate-Form/releases/tag/1.0)
- Floodgate



[Example](https://github.com/zimzaza4/Skript-Floodgate-Form/wiki/Example)

Create a Form:
```
set {_Form} to simple form with title "hello"
set {_Form} to modal form with title "hello" and buttons "button1" "button2"
set {_Form} to custom form with title "hello"
```

Add button to a Simple Form:
```
add button display "button" to form {_simpleform}
add button display "button with url image" with url icon "url" to form {_simpleform}
add button display "button with path image" with path icon "path" to form {_simpleform}
```
content
```
add content "content" to {_Form}
```
Send Form:
```
send-form {_Form} with id "Form_id" to {_player}
```
Events:

  on Click Form Button:   (ModalForm and SimpleForm)
```
on click form button:
    set {_id} to data "form-id"
    set {_button} to data "button-id"
```
  on Submit Custom Form:   (CustomForm)
```
on submit custom form:
    set {_id} to data "form-id"
    set {_input} to input component id 0 of data "response"
```
(一些语法懒得补了，自己翻吧)
Recommendation:
 Use Floodgate-Skript to detect bedrock players
