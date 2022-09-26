---
layout: post
title:  "Getting my hands dirty with Kotlin"
date:   2022-09-18 14:00:00 +0900
categories: Android Studio
---

## Introduction

## View

## XML

```XML
<?xml version="1.0" encoding="utf-8"?>
<androidx.constraintlayout.widget.ConstraintLayout xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:app="http://schemas.android.com/apk/res-auto"
    xmlns:tools="http://schemas.android.com/tools"
    android:background="@color/test"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    tools:context=".MainActivity">

    <ImageView
        android:id="@+id/imageView"
        android:layout_width="200dp"
        android:layout_height="200dp"
        app:layout_constraintStart_toStartOf="parent"
        app:layout_constraintEnd_toEndOf="parent"
        app:layout_constraintTop_toTopOf="parent"
        android:layout_marginTop="200dp"
        android:src="@drawable/ic_picasso"
         />

    <TextView
        android:id="@+id/textView2"
        android:layout_width="180dp"
        android:layout_height="38dp"
        android:gravity="center"
        android:text="Hi! I am Blah"
        android:textSize="20sp"
        android:textColor="@color/white"
        app:layout_constraintEnd_toEndOf="parent"
        app:layout_constraintStart_toStartOf="parent"
        app:layout_constraintTop_toBottomOf="@+id/imageView"
        android:layout_marginTop="50dp"
        />

    <androidx.appcompat.widget.AppCompatButton
        android:id="@+id/button"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:text="LIKE"
        app:layout_constraintTop_toBottomOf="@id/textView2"
        android:layout_marginTop="40dp"
        app:layout_constraintStart_toStartOf="parent"
        app:layout_constraintEnd_toEndOf="parent"
        app:layout_constraintHorizontal_bias="0.3"
        android:background="@drawable/button_background"
 />

    <androidx.appcompat.widget.AppCompatButton
        android:id="@+id/button2"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:text="HATE"
        android:textColor="@color/white"
        app:layout_constraintTop_toBottomOf="@id/textView2"
        android:layout_marginTop="40dp"
        app:layout_constraintEnd_toEndOf="parent"
        android:layout_marginEnd="100dp"
        android:background="@color/green"

 />

</androidx.constraintlayout.widget.ConstraintLayout>

```

Text view:
Image view:
button:
parent: frame that contains

#### layout

- constraint
  - constraintTop: designate the top of View to
    - constraintTop_toTopOf: the top of @id/parent
    - constraintTop_toBottomof: the botton of @id/parent
  - constraintBottom: designate the bottom of View to
    - constraintBottom_toTopOf: the top of @id/parent
    - constraintBottom_toBottomof: the bottom of @id/parent
  - constraintStart: designate the start of View to
    - constraintStart_toStartOf: the start of @id/parent
    - constraintStart_toEndof: the end of @id/parent
  - constraintEnd: designate the bottom of View to
    - constraintEnd_toStartOf: the start of @id/parent
    - constraintEnd_toEndof: the end of @id/parent
- margin: only 0 or positive value
  - android:layout_marginStart
  - android:layout_marginEnd
  - android:layout_marginTop
  - android:layout_marginBottom
- bias: value between 0 to 1
  - layout_constraintHorizontal_bias
  - layout_constraintVertical_bias

#### color

- values/colors.xml

    ```xml
    <?xml version="1.0" encoding="utf-8"?>
    <resources>
    <color name="black">#FF000000</color>
    <color name="white">#FFFFFFFF</color>
    <color name="green">#8BC34A</color>
    <color name="red">#F44336</color>
    <color name="test">#2760D5</color>
    <color name="yellow">#FFFF00</color>
    <color name="bantumyeongyellow">#50FFFF00</color>
    </resources>
    ```

- 6-number color: #FFFFFF
    first two Hexadecimal numbers: Red
    middle two Hexadecimal numbers: Green
    last two Hexadecimal numbers: Blue
    (example: FF00FF is purple as this color is composed with 256 amount of Red, 0 amount of Green, 256 amount of Blue)

- 8-number color: #30FFFFFF
    first two digits represent the transparancy of color
    following six digits resembles the 6-number color

#### size

```xml
    android:layout_marginTop="40dp"
    android:textSize="20sp"
```

- dp: Density-Independent Pixels, dp는 화면에 따라 사이즈가 달라지지 않고 고정된 값을 갖는다.

- sp: Scale-Independent Pixels, sp는 시스템의 사이즈에 따라 TextView가 작아지거나 커진다.

## Image

![design2](/devblog/assets/android%20store/design2.png)

## Kotlin

Car.Kt

```kotlin
package com.example.myapplication

class Car {
    var color = "red"
    var speed1 = 0.0f
    var speed2 = 1
    var model = "porche"
    fun accelerate(maxSpeed: Int){
        speed2 = maxSpeed
    }

    fun brake(){
        speed2 = 0
    }
}
```

- var: variable, data type that data could change
- val: value, data type that data does not change
- fun: function, if using data outside function, should call(data type should be written)

ExampleUnitTest.Kt

```kotlin
package com.example.myapplication

import org.junit.Test

import org.junit.Assert.*

/**
 * Example local unit test, which will execute on the development machine (host).
 *
 * See [testing documentation](http://d.android.com/tools/testing).
 */
class ExampleUnitTest {

    var myCar = Car()

    @Test
    fun addition_isCorrect() {
        var currentSpeed = myCar.speed2
        println("@@@@@@@@@@@@@@@@@@@@@$currentSpeed")

        myCar.accelerate(100)

        currentSpeed = myCar.speed2
        println("@@@@@@@@@@@@@@@@@@@@@$currentSpeed")

        assertEquals("green", myCar.color)
    }
}

```

- escape of string = $

## Conclusion
