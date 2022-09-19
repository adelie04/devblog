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
    android:background="@color/purple_200"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    tools:context=".MainActivity">

    <ImageView
        android:id="@+id/imageView"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        app:layout_constraintStart_toStartOf="parent"
        app:layout_constraintEnd_toEndOf="parent"
        app:layout_constraintTop_toTopOf="parent"
        android:layout_marginTop="200dp"
        tools:srcCompat="@tools:sample/avatars" />

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

    <Button
        android:id="@+id/button"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:text="LIKE"
        app:layout_constraintTop_toBottomOf="@id/textView2"
        android:layout_marginTop="40dp"
        app:layout_constraintStart_toStartOf="parent"
        android:layout_marginStart="100dp"

 />

    <Button
        android:id="@+id/button2"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:text="HATE"
        android:textColor="@color/white"
        app:layout_constraintTop_toBottomOf="@id/textView2"
        android:layout_marginTop="40dp"
        app:layout_constraintEnd_toEndOf="parent"
        android:layout_marginEnd="100dp"

 />


</androidx.constraintlayout.widget.ConstraintLayout>

    // android:rotationX="90" 배경이 돌아가더라

```

## Image

![design1](/devblog/assets/android%20store/design1.png)

## Conclusion
