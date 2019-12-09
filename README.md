# ScrollView-Tutorial
This is a tutorial on how to use ScrollView in Android Studio. This tutorial contains an explanation along with the demo app which can help in a simple implementation of ScrollView in an Android Studio project. 

## Introduction
ScrollView is a view group that allows the vertical scrolling of the hierarchy placed within it. It is generally used for the content which exceeds the regular size of the screen display or the other layouts like linearlayout, relativelayout, framelayout, and more. Its implementation is provided from the android.widget.ScrollView class and android considers it the default scroll view.

ScrollView can only contain one direct child. To add multiple views inside it, another type of standard layout (LinearLayout, RelativeLayout, etc) must be included inside it first and only then other views can be added.

However, ScrollView only allows vertical scrolling. HorizontalScrollView class is used in order to implement horizontal scrolling in the application.

A word of caution!; Never use a RecyclerView, a Gridview or a ListView within a Scrollview because this can result in the app preforming poorly. The reason behind this is that all these views have their own scrolling inside them.

## History
ScrollView was released with API level 1 and has been a part of Android development since day one. 

It belongs to android.widget.ScrollView class which is extended from the android.widget.FrameLayout class.

## Attributes

Some of the main attributes of ScrollView are:-

(These attributes are included in the XML files with the android tag.) 

| Attribute     | Definition                                                                                                                                                                                                                                      |
|---------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| id            | The id attribute in android studio is used to uniquely identify ScrollView and can be used in the java code by 
assigning it to a variable which is defined by the findViewByID method. This variable can then be used to manipulate ScrollView. |
| fillViewport  | In Android development, fillViewport can be used to stretch ScrollView's content to fill the viewport. Its value is in boolean that is either true or false.                                                                                   |
| layout_width  | This is used to specify the width of ScrollView.                                                                                                                                                                                                |
| layout_height | This is used to specify the height of ScrollView.                                                                                                                                                                                               |

It is important to remember that while specifying a numeric value of layout_width and layout_height, don't forget to append the unit to it. The units that are available to use with these attributes are px (pixels), dp (density-independent pixels), sp (scaled pixels based on preferred font size), in (inches), and mm (millimeters).

## Code Output
Down below is the app code, provided in this repository, running in the android studio emulator. It has a ScrollView which contains a LinearLayout. This LinearLayout helps in adding multiple views inside it. This app has two TextViews and two buttons which are larger than the screen size and can be scrolled.
<img src="Images/emulator.gif" width="400" height="600" align="middle" alt="Emulator">

## Example 
To implement a ScrollView, no java coding is required. All ScrollView attributes are contained within the activity's XML layout file. 

* To begin with, create a new Android project or use your own. In the code given below, a new project was created and an empty activity was chosen. It had a MainActivity.java file which was left untouched and an XML layout file that contained all the coding.

* Then going into the XML layout file, go to the Design tab and drag and drop the ScrollView from Containers list to the user interface (UI).

* Go to the Text tab and you will see some code inside the ScrollView tag. Add or manipulate different tags until you get the desired result. An example of the code is shown below. This code makes the use of all the attributes given above.

```XML
//This is the tag ScrollView and it contains all the attributes
 <ScrollView
        android:id="@+id/scrollView"
        android:layout_width="391dp"
        android:layout_height="562dp"
        app:layout_constraintBottom_toBottomOf="parent"
        app:layout_constraintEnd_toEndOf="parent"
        app:layout_constraintStart_toStartOf="parent"
        app:layout_constraintTop_toTopOf="parent"
        android:fillViewport="false"/>
 ```
 * Inside the ScrollView, you need to add another layout like Linearlayout if you want multiple children inside it. In the case of multiple children, they can be dragged inside the nested layout then after. An example of the code given below shows a LinearLayout which is embedded in ScrollView and has multiple views like TextView and Buttons inside it.
 
 ```XML
//This is the linear layout which is embedded inside ScrollView to allow multiple children views
        <LinearLayout
            android:layout_width="match_parent"
            android:layout_height="wrap_content"
            android:orientation="vertical">
//The various views inside LinearView and hence, ScrollView
            <TextView
                android:id="@+id/textView3"
                android:layout_width="match_parent"
                android:layout_height="wrap_content"
                android:text="@string/Text1"
                android:textSize="22dp" />

            <Button
                android:id="@+id/button3"
                android:layout_width="match_parent"
                android:layout_height="wrap_content"
                android:text="Button" />

            <TextView
                android:id="@+id/textView4"
                android:layout_width="match_parent"
                android:layout_height="wrap_content"
                android:text="@string/Text2"
                android:textSize="22dp" />

            <Button
                android:id="@+id/button4"
                android:layout_width="match_parent"
                android:layout_height="wrap_content"
                android:text="Button" />
        </LinearLayout> //Closing tag of the LinearLayout
```
## References 
