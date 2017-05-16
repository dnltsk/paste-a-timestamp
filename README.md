# paste-a-timestamp
`^⌘U` - because life's too short to type ISO-8601 timestamps manually

## usage

Writing timestamps is annoying - especially when you often need to type the timestamp of _now_. 
After installing the script and configuring the shortcut you can use 
`^⌘u` (`Control`+`Command`+`U`) to pasted the current timestamp into the cursor's position.

![usage](meta-inf/usage.gif)


## requirements

1. OSX (tested with 10.12 - Sierra) 

## setup

### part 1 - create a service

1. open the `Automator` application
2. create a new `Service` via menu `File`, `New`
3. configure `Service Reveives` to `no input`
4. drag the `Run AppleScript` action into the right area<br> 
![automator-1](META-INF/automator-1.jpg)
5. copy-paste the content of [paste-a-timestamp.scpt](paste-a-timestamp.scpt) snippet into the AppleScript<br>
![automator-2](META-INF/automator-2.jpg)
6. save the AppleScript as `paste-a-timestamp` via menu `File`, `Save`

### part 2 - configure the shortcut

1. open the `Keybord` settings under `System Preference`
2. in tab `Shortcuts` search for the `paste-a-timestamp` service
3. double-click on the `none` text to record the shortcut you want to use - e.g. `^⌘U` (`Control`+`Command`+`U`)<br>
![keyboard-1](META-INF/keyboard.jpg)

### part 3 - allow interaction
 
1. open the `Security & Privacy` settings under `System Preference`
2. in tab `Privacy` and setting `Accessibility` allow the `Automator` application to control your computer<br>
Therefore open the lock in the lower-left corner<br>
![keyboard-1](META-INF/privacy.jpg)

## troubleshooting

* after the setup process it may **need some minutes** until it works until it works in all applications - for whatever reason
* **the shortcut will not work** in an application that overwrites it - Then you have to change the *paste-a-timestamp* shortcut 
or reconfigure the application 