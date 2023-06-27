Ex.No-2-To-develop-an-application-that-uses-GUI-Components-with-Fonts-and-Colors.

AIM:

To create an application that uses GUI Components with Fonts and Colors using Android Studio.

EQUIPMENTS REQUIRED:

Latest Version Android Studio

ALGORITHM:

PROGRAM:

/*

Program to print the text “GUIcomponent”.

Developed by: Arun Karthik.V

Registeration Number : 212221040018

*/

activity_main.xml

<?xml version="1.0" encoding="utf-8"?>

<androidx.constraintlayout.widget.ConstraintLayout xmlns:android="http://schemas.android.com/apk/res/android"

    xmlns:app="http://schemas.android.com/apk/res-auto"
    
    xmlns:tools="http://schemas.android.com/tools"
    
    android:layout_width="match_parent"
    
    android:layout_height="match_parent"
    
    tools:context=".MainActivity">
    
    <TextView
    
        android:id="@+id/textView"
        
        android:layout_width="match_parent"
        
        android:layout_height="wrap_content"
        
        android:layout_margin="30dp"
        
        android:layout_marginTop="296dp"

        android:gravity="center"
        
        android:text="Change Color"
        
      app:layout_constraintBottom_toBottomOf="parent" 
      
      app:layout_constraintStart_toStartOf="parent" 
      
      app:layout_constraintTop_toBottomOf="@+id/fontButton" 
      
      app:layout_constraintVertical_bias="0.082" />

<Button
  
android:id="@+id/fontButton"

  android:layout_width="wrap_content" 
  
  android:layout_height="wrap_content" 
  
  android:layout_below="@id/colorButton" 
  
  android:layout_centerHorizontal="true" 
  
  android:layout_marginStart="120dp" 
  
  android:layout_marginTop="120dp" 
  
  android:text="Change Font" 
  
  app:layout_constraintStart_toStartOf="parent"
  
  app:layout_constraintTop_toBottomOf="@+id/textView" />

<TextView
android:id="@+id/textView" 
  
android:layout_width="wrap_content" 

android:layout_height="wrap_content" 

android:layout_below="@id/fontButton"

android:layout_centerHorizontal="true" 

android:text="Hello World!" 

android:textSize="40sp" 

app:layout_constraintBottom_toBottomOf="parent" 

app:layout_constraintEnd_toEndOf="parent" 

app:layout_constraintHorizontal_bias="0.435"

app:layout_constraintStart_toStartOf="parent"

app:layout_constraintTop_toTopOf="parent" 

app:layout_constraintVertical_bias="0.325" />

</androidx.constraintlayout.widget.ConstraintLayout>

MainActivity.java

package com.example.myapplication;	

import androidx.appcompat.app.AppCompatActivity;

import android.graphics.Color; 

import android.graphics.Typeface; 

import android.os.Bundle;

import android.view.View; 

import android.widget.Button; 

import android.widget.TextView;

public class MainActivity extends AppCompatActivity { 

private Button colorButton;

private Button fontButton; 

private TextView textView; 

@Override

protected void onCreate(Bundle savedInstanceState) { 

super.onCreate(savedInstanceState); 

setContentView(R.layout.activity_main); 

colorButton = findViewById(R.id.colorButton); 

fontButton = findViewById(R.id.fontButton); 

textView = findViewById(R.id.textView);

colorButton.setOnClickListener(new View.OnClickListener() { 

@Override

public void onClick(View v) {

changeTextColor();

} });

fontButton.setOnClickListener(new View.OnClickListener() { 

@Override

public void onClick(View v) {

changeFont();

}

});

}

private void changeTextColor() { 

int randomColor = Color.rgb(

(int) (Math.random() * 256),
 
(int) (Math.random() * 256),

(int) (Math.random() * 256)

);

textView.setTextColor(randomColor);

}

private void changeFont() {

Typeface[] fontStyles = new Typeface[]{

Typeface.DEFAULT
, 
Typeface.DEFAULT_BOLD,

Typeface.MONOSPACE,

Typeface.SANS_SERIF,

Typeface.SERIF

};

int randomIndex = (int) (Math.random() * fontStyles.length); 

Typeface selectedFont = fontStyles[randomIndex]; 

textView.setTypeface(selectedFont);}

}

OUTPUT

![image](https://github.com/Karthik2821/Ex.No-2-To-develop-an-application-that-uses-GUI-Components-with-Fonts-and-Colors./assets/134921933/3e07f839-71ba-4542-aff6-10be24571a25)

![image](https://github.com/Karthik2821/Ex.No-2-To-develop-an-application-that-uses-GUI-Components-with-Fonts-and-Colors./assets/134921933/f6b38a13-7007-478a-b68d-ba71ec696b85)

![image](https://github.com/Karthik2821/Ex.No-2-To-develop-an-application-that-uses-GUI-Components-with-Fonts-and-Colors./assets/134921933/756b67c4-1d20-43bf-814c-734534b863a2)

![image](https://github.com/Karthik2821/Ex.No-2-To-develop-an-application-that-uses-GUI-Components-with-Fonts-and-Colors./assets/134921933/6e6c4cd0-c52d-4e24-935c-5a21457ee0da)

RESULT

Thus a Simple Android Application that uses GUI Components with Fonts and Colors using Android Studio is developed and executed successfully.
































        
