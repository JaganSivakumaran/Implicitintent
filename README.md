# Ex.No:3 Develop program to create a text field and a button “Navigate”. When you enter “www.google.com” and press navigate button it should open google page using Implicit Intents.


## AIM:

To create a navigate button using Implicit Intent to display the google page using Android Studio.

## EQUIPMENTS REQUIRED:

Latest Version Android Studio

## ALGORITHM:



## PROGRAM:
```
/*
Program to print the text “Implicitintent”.
Developed by: Jagan S
Registeration Number : 21222104
*/

## activity_main.xml

<?xml version="1.0" encoding="utf-8"?>
<androidx.constraintlayout.widget.ConstraintLayout
xmlns:android="http://schemas.android.com/apk/res/android"
xmlns:app="http://schemas.android.com/apk/res-auto"
xmlns:tools="http://schemas.android.com/tools"
android:layout_width="match_parent"
android:layout_height="match_parent"
tools:context=".MainActivity">
<Button
android:id="@+id/button"
android:layout_width="wrap_content"
android:layout_height="wrap_content"
android:layout_marginEnd="48dp"
android:text="NAVIGATE"
app:layout_constraintBottom_toBottomOf="parent"
app:layout_constraintEnd_toEndOf="parent"
app:layout_constraintTop_toTopOf="parent"
app:layout_constraintVertical_bias="0.219" />
<EditText
android:id="@+id/editTextTextPersonName"
android:layout_width="wrap_content"
android:layout_height="wrap_content"
android:layout_marginStart="32dp"
android:ems="10"
android:inputType="textPersonName"
app:layout_constraintBottom_toBottomOf="parent"
app:layout_constraintStart_toStartOf="parent"
app:layout_constraintTop_toTopOf="parent"
app:layout_constraintVertical_bias="0.218" />
</androidx.constraintlayout.widget.ConstraintLayout>


## MainActivity.java:

package com.example.ex3;
import androidx.appcompat.app.AppCompatActivity;
import android.content.Intent;
import android.net.Uri;
import android.widget.Button;
import android.widget.EditText;
import android.os.Bundle;
public class MainActivity extends AppCompatActivity {
Button button;
EditText editText;
@Override
protected void onCreate(Bundle savedInstanceState) {
super.onCreate(savedInstanceState);
setContentView(R.layout.activity_main);
button = findViewById(R.id.button);
editText = findViewById(R.id.editTextTextPersonName);
button.setOnClickListener(view -> {
String url=editText.getText().toString();
Intent intent=new Intent(Intent.ACTION_VIEW, Uri.parse(url));
startActivity(intent);
});
} }

```

## OUTPUT

![image](https://github.com/JaganSivakumaran/Implicitintent/assets/134905062/955b32ca-86c8-422d-916c-3de42146566e)

![image](https://github.com/JaganSivakumaran/Implicitintent/assets/134905062/670ba8b6-104d-4730-bdb9-1493176fd99c)






## RESULT
Thus a Simple Android Application create a navigate button using Implicit Intent to display the google page using Android Studio is developed and executed successfully.
