# Skript-Floodgate-Form
A simple skript




The skript depends on plugins:
- Skript
- Skript-Reflect
- BEMenuAPI
- Floodgate(2.0)



#Example

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
add button display "button with path image" with path image "path" to form {_simpleform}
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


