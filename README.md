
# cordova-plugin-dialogs-types

This plugin is exactly the same as "https://github.com/apache/cordova-plugin-dialogs" except `navigator.notification.prompt`.


## Installation

    cordova plugin add https://github.com/laelbe/cordova-plugin-dialogs-types.git


## navigator.notification.prompt

Displays a native dialog box that is more customizable than the browser's `prompt` function.

    navigator.notification.prompt(message, promptCallback, [title], [buttonLabels], [defaultText], [inputType])

- __message__: Dialog message. _(String)_

- __promptCallback__: Callback to invoke with index of button pressed (1, 2, or 3) or when the dialog is dismissed without a button press (0). _(Function)_

- __title__: Dialog title _(String)_ (Optional, defaults to `Prompt`)

- __buttonLabels__: Array of strings specifying button labels _(Array)_ (Optional, defaults to `["OK","Cancel"]`)

- __defaultText__: Default textbox input value (`String`) (Optional, Default: empty string)

- __inputType__: Textbox input type (`String`) (Optional, Default: 'text'. Valid values : 'text', 'password', 'number')



### Example

    function onPrompt(results) {
        alert("You selected button number " + results.buttonIndex + " and entered " + results.input1);
    }

    navigator.notification.prompt(
        'Please enter your name',  // message
        onPrompt,                  // callback to invoke
        'Registration',            // title
        ['Ok','Exit'],             // buttonLabels
        'Jane Doe',                // defaultText
        'password'                 // inputType
    );


### Preview

#### IOS
![IOS Preview](https://github.com/laelbe/cordova-plugin-dialogs-types/blob/master/doc/demo-ios.gif?raw=true)

#### Android
![Android Preview](https://github.com/laelbe/cordova-plugin-dialogs-types/blob/master/doc/demo-android.gif?raw=true)



