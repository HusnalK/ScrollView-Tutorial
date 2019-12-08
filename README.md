# ScrollView-Tutorial
This is a tutorial on how to use ScrollView in Android Studio. This tutorial contains explanation along with the a demo app which can help in simple implementation of ScrollView in an Android Studio project.
## Introduction
ScrollView is a view group which allows the vertical scrolling of the hierarchy placed within it. It is generally used for content which exceeds the regular size of the other layouts or the screen display. It's implementation is provided from the android.widget.ScrollView class and android considers it the default scroll view.
ScrollView can only contain one direct child. To add multiple views inside it, another type of standard layout (linearLLayout, relativeLayout, etc) must be included inside it first and only then other views can be added.
However, since it only allows vertical scrolling, HorizontalScrollView is used to implement horizontal scrolling.
## History
ScrollView was released with API level 1 and is part of android.widget.ScrollView class which is extended from the android.widget.FrameLayout class. 
