# Android Custom Accordion
Custom accordion for android developers

Android has no built-in accordion view, so that you can use this approach to easly create custom accordions.

# How to use?

There are 2 files. Java code for Activity and XML file for layout.
You don't need to edit Java code. It will handle one ore more accordions as you create them useing XML layout file.
I have added XML file with 3 accordion elements. You must copy following code and paste it after last accordion element in parent LinerLayout You need only change Accordion header and text. Icon files must be placed in drawable folder.

```

<View <!-- Divider line between accordion elements, no need for first one -->
    android:layout_width="match_parent"
    android:layout_height="1dp"
    android:background="#ccc"/>

<LinearLayout
    android:onClick="toggleAccordion" <!-- method will be invoked whihin Activity Java code -->
    android:layout_width="match_parent"
    android:layout_height="wrap_content"
    android:orientation="horizontal"
    android:padding="10dp">

    <TextView <!-- Accordion element header text -->
        android:layout_width="0dp"
        android:layout_height="wrap_content"
        android:layout_weight="1"
        android:text="Accordion Element Header"
        android:textSize="24sp" />

    <ImageView <!-- Image for arrows -->
        android:layout_width="24dp"
        android:layout_height="24dp"
        android:layout_gravity="center_vertical"
        android:background="@drawable/icon_down"
        android:textSize="24sp" />

</LinearLayout>

<TextView <!-- Accordion text -->
    android:visibility="gone"
    android:text="It is an accordion text"
    android:padding="10dp"
    android:layout_width="match_parent"
    android:layout_height="wrap_content" />
    
 ```
