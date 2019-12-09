# ScrollView-Tutorial
This is a tutorial on how to use ScrollView in Android Studio. This tutorial contains an explanation along with the demo app which can help in a simple implementation of ScrollView in an Android Studio project. 

## Introduction
ScrollView is a view group that allows the vertical scrolling of the hierarchy placed within it. It is generally used for the content which exceeds the regular size of the screen display or the other layouts like linearlayout, relativelayout, framelayout, and more. Its implementation is provided from the android.widget.ScrollView class and android considers it the default scroll view.

ScrollView can only contain one direct child. To add multiple views inside it, another type of standard layout (linearLayout, relativeLayout, etc) must be included inside it first and only then other views can be added.

However, ScrollView only allows vertical scrolling. HorizontalScrollView class is used in order to implement horizontal scrolling in the application.

A word of caution!; Never use a RecyclerView, a Gridview or a ListView within a Scrollview because this can result in the app preforming poorly. The reason behind this is that all these views have their own scrolling inside them.

## History
ScrollView was released with API level 1 and has been contained within Android development since day one. 

It is part of android.widget.ScrollView class which is extended from the android.widget.FrameLayout class.

