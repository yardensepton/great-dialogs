# Great Dialogs :left_speech_bubble:	

Great dialogs is an Android library that provides customizable dialog options to enhance user interactions in your app.
Choose from three types of dialogs: success, error, and question.
Each dialog comes with a Lottie animation and various customization options.

## Features:
1. Dialog Types: Success, Error, and Question.
2. Customizable Title and Message: Design the text and colors.
3. Customizable Buttons: Choose text, colors, and button configurations (Cancel or OK button, or both!).
4. Lottie Animations: Each dialog includes a Lottie animation.
5. Optional Vibration: Enable vibration when the dialog is shown, if not chosen - the default is no vibration.
6. Button Click Listeners: Add onClick functions to the buttons.

## Installation:
1. Add the following dependency to your build.gradle file:
```
dependencies {
    implementation 'com.example.greatdialogs:greatdialogs:1.0.1'
    implementation("com.airbnb.android:lottie:4.1.0")
}
```
2. Add the following permission to your AndroidManifest.xml file:

```
<uses-permission android:name="android.permission.VIBRATE"/>
```
## Usage:

Example of an error dialog :triangular_flag_on_post:	

```
            GreatDialog dialog = new GreatDialog(MainActivity.this, DialogType.ERROR);
            dialog.setTitle("ERROR")
                    .setVibrate(true)
                    .setButtonVisibility(ButtonNames.OK, true)
                    .setButtonVisibility(ButtonNames.CANCEL,false)
                    .setMessage("We are sorry, please try again!")
                    .setOKButtonText("OK")
                    .setOkButtonColor(Color.RED)
                    .setTitleColor(Color.BLACK)
                    .setMsgColor(Color.BLACK)
                    .setOKButtonOnClickListener(this::performCustomAction).show();
```

Example of a success dialog: :heavy_check_mark:	

```
 GreatDialog dialog = new GreatDialog(MainActivity.this, DialogType.SUCCESS);
            dialog.setTitle("SUCCESS")
                    .setButtonVisibility(ButtonNames.OK, true)
                    .setButtonVisibility(ButtonNames.CANCEL,false)
                    .setMessage("Yay you did it!")
                    .setOKButtonText("OK")
                    .setOkButtonColor(Color.GREEN)
                    .setOkButtonTextColor(Color.BLACK)
                    .setTitleColor(Color.BLACK)
                    .setMsgColor(Color.BLACK)
                    .setOKButtonOnClickListener(this::performCustomAction).show();
```

Example of a question dialog :warning:	

```
GreatDialog dialog = new GreatDialog(MainActivity.this, DialogType.QUESTION);
            dialog.setTitle("WARNING")
                    .setButtonVisibility(ButtonNames.OK, true)
                    .setButtonVisibility(ButtonNames.CANCEL,true)
                    .setMessage("Are you sure you want to delete?")
                    .setOKButtonText("OK")
                    .setCancelButtonColor(Color.GRAY)
                    .setOkButtonColor(Color.RED)
                    .setCancelButtonTextColor(Color.WHITE)
                    .setTitleColor(Color.BLACK)
                    .setMsgColor(Color.BLACK)
                    .setOKButtonOnClickListener(this::performCustomAction).show();
```

## Preview :movie_camera:	

https://github.com/yardensepton/GreatDialogs/assets/98481395/5d786139-f40f-42da-a1ba-0dc7f0275230











