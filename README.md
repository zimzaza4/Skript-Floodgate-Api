# Skript-Floodgate-Api

Floodgate Api for Skript


**How to install?** 
- After confirming to install all dependent plugins, put this script into plugins/Skript/scripts/ and reload it


**如何安装?**
- 装上Skript, [Skript-Reflect](https://github.com/TPGamesNL/skript-reflect/releases) 插件
- 将该脚本放入该放的文件夹 plugins/Skript/scripts/
- 启动服务器


The skript depends on plugins:
- [Skript](https://github.com/SkriptLang/Skript/releases)
- [Skript-Reflect](https://github.com/TPGamesNL/skript-reflect/releases)
- [Floodgate](https://ci.opencollab.dev/job/GeyserMC/job/Floodgate/job/master/)



[Example](https://github.com/zimzaza4/Skript-Floodgate-Form/wiki/Example)

Create a Form:
```
set {_Form} to simple form with title "hello"
set {_Form} to modal form with title "hello" and buttons "button1" "button2"
set {_Form} to custom form with title "hello"
```

Add something to a Simple Form:
```
add button display "button" to form {_simpleform}
add button display "button with url image" with url icon "url" to form {_simpleform}
add button display "button with path image" with path icon "path" to form {_simpleform}
add content "content" to form {_Form}
```
Send Form:
```
send form {_Form} to {_player}
send form {_Form} with id "Form_id" to {_player}
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

*You don't need Floodgate-Skript any more*

Extra:
NPC Form
[GeyserUtils](https://github.com/zimzaza4/GeyserUtils
