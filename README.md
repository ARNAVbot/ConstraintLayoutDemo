# ConstarinLayoutDemo
Demo app to show various utilities of Constraint Layout.
To add depedency of constraint layout in your project , do the following:
1. Ensure you have the maven.google.com repository declared in your top-level build.gradle file:
```
repositories {
    google()
}
```
2. Add the library as a dependency in the module-level build.gradle file, as shown in the following example. Note that the latest version might be different than what is shown in the example:
```
dependencies {
    implementation "androidx.constraintlayout:constraintlayout:2.0.4"
}
```
3. In the toolbar or sync notification, click Sync Project with Gradle Files.


This repo will basically help in getting familiar with some of the basic and dialy use concepts of Constraint Layout that developers generally use in their day-to-day life.

Following topics will be covered in this repo:
1. Autoconnect tool
2. Constraint Bias
3. Changing elements layout_width and layout_height
4. Pack tool and Infer Consteaints tool
5. Barriers
6. Chains (https://developer.android.com/training/constraint-layout/index.html#constrain-chain)

Let's get started
1. Autoconnect tool
2. what does scale type mean android
 
3. The measure of space between the element and the layout's border is known as the constraint bias.
 
If the element is centered, its constraint bias is 50%, which means the element is halfway between the two borders. If the bias is changed to 30% for horizontal constraints, the element would be placed closer to the left border. If it is changed to 70%, the element would be placed closer to the right border. The same is true of vertical constraints: the bias controls how far the element is from the top and bottom borders.
After adding two opposing horizontal constraints—a left and a right constraint—a horizontal slider appears in the view inspector to adjust the bias of the element along the horizontal axis. If you add two opposing vertical constraints, a vertical slider appears to adjust the vertical bias.
 
4.Change the element's layout width and height
The inner lines within the view inspector let you change the UI element's layout_width and layout_height values relative to constraints. Clicking an inner line cycles through the following options for vertical and horizontal constraints:

Fixed: <img width="24" alt="Screenshot 2021-02-14 at 5 23 34 PM" src="https://user-images.githubusercontent.com/8524951/107876031-6c662180-6ee9-11eb-905d-91cbf4de245b.png">

Specify the width/height of the element.

Match Constraints: <img width="37" alt="Screenshot 2021-02-14 at 5 21 56 PM" src="https://user-images.githubusercontent.com/8524951/107875977-2d37d080-6ee9-11eb-998f-2eeb785f2f04.png">

Allow the element to occupy all available space to satisfy the constraint. (Note that this is not the same as the match_parent value for width or height, which sets the element to occupy all available space of the parent view. You shouldn't use match_parent for any view in a ConstraintLayout.) In the XML file, the value 0dp appears in the layout_width or layout_height attribute for Match Constraints.


Wrap Content: <img width="28" alt="Screenshot 2021-02-14 at 5 24 31 PM" src="https://user-images.githubusercontent.com/8524951/107876054-84d63c00-6ee9-11eb-870d-1327fbc31bc7.png">

Expand the element as needed to fit its content.
 
5.By using a baseline constraint, you can vertically align elements that have text, such as a TextView, EditText, or Button, so that the text baselines are aligned. Use baseline constraints to align elements that use different text sizes. Baseline constraints are also useful for aligning the text baselines of elements of different sizes.
Refer [this](https://developer.android.com/codelabs/constraint-layout#7) doc for the above thing 
 
6. to expand an element horizontally and vertically using the Pack  tool, <img width="41" alt="Screenshot 2021-02-14 at 5 25 25 PM" src="https://user-images.githubusercontent.com/8524951/107876081-a8998200-6ee9-11eb-9c6d-3cc2196ecfe5.png">
and how to use the Infer Constraints  tool <img width="37" alt="Screenshot 2021-02-14 at 5 25 30 PM" src="https://user-images.githubusercontent.com/8524951/107876091-bfd86f80-6ee9-11eb-8966-db3e485a3da7.png">
. Both tools are in the toolbar at the top of the Layout Editor.
 
7. The Infer Constraints tool infers, or figures out, the constraints you need to match a rough layout of elements. It works by taking into account the positions and sizes of the elements. Drag elements to the layout in the positions you want them, and use the Infer Constraints tool to automatically create the constraint connections.
 
8. What's the difference between Inference and Autoconnect?
The Infer Constraints tool calculates and sets constraints for all of the elements in a layout, rather than just the selected element. It bases its calculations on inferred relationships between the elements.
The Autoconnect  tool <img width="35" alt="Screenshot 2021-02-14 at 5 26 48 PM" src="https://user-images.githubusercontent.com/8524951/107876101-d5e63000-6ee9-11eb-90cb-63d453f33776.png">
creates constraint connections for a selected element to the element's parent.
9. Refer to [this](https://developer.android.com/codelabs/constraint-layout#8) for above
10. You can quickly resize elements by aspect ratio if at least one of the element's dimensions is set to match constraints. Check [this](https://developer.android.com/codelabs/constraint-layout#9)
11.  Use barriers to align elements that dynamically vary in size
Barriers allow you to specify a constraint based on multiple UI elements. You'll want to use barriers any time that multiple elements could dynamically change their size based on user input or language.
 
A constraint to a barrier is just like a constraint to another element. However, users don't see barriers, and barriers don't add a level to the app's view hierarchy, which means they don't affect performance.
Refer to [this](https://developer.android.com/codelabs/constraint-layout#10)
 
12. Use chains to position multiple elements
You've already learned how to center a single UI element. In this exercise you will learn how to center multiple elements at once using a chain. A chain is a group of elements that are linked to each other with bi-directional position constraints.
When you create a chain, you can position all of the elements as a group, and center all of your chained elements as if they were a single element. Refer [this](https://developer.android.com/codelabs/constraint-layout#11)
13. There is also a button in the toolbar which helps to delete all the constraints in 1 go.<img width="39" alt="Screenshot 2021-02-14 at 5 30 08 PM" src="https://user-images.githubusercontent.com/8524951/107876169-53aa3b80-6eea-11eb-84ab-96a10fad89d8.png">


14. Similar to a guideline, a barrier is an invisible line that you can constrain views to. Except a barrier does not define its own position; instead, the barrier position moves based on the position of views contained within it. This is useful when you want to constrain a view to the a set of views rather than to one specific view.


## TODO's
1. Use guideline -> You can add a vertical or horizontal guideline to which you can constrain views, and the guideline will be invisible to app users. You can position the guideline within the layout based on either dp units or percent, relative to the layout's edge.

2. Keyframe animations -> https://developer.android.com/training/constraint-layout/index.html#keyframe_animations

## What's next ?
1. Motion Layout -> https://github.com/android/views-widgets-samples/tree/main/ConstraintLayoutExamples


## Imp articles
1. https://www.youtube.com/watch?v=rzmB3UxxhaA
2. https://proandroiddev.com/constraintlayout-vs-other-layouts-a-battle-towards-performance-part-1-14d8116e876e
3. https://proandroiddev.com/constraintlayout-vs-other-layouts-a-battle-towards-performance-part-2-21d6b5a6054c
4. https://nik-arora8059.medium.com/a-battle-towards-performance-constraintlayout-vs-other-layouts-part-3-d7646a849b4e
5. https://android.jlelse.eu/constraint-layout-performance-870e5f238100
6. https://medium.com/@sasanksunkavalli/android-constraintlayout-layout-constraintdimensionratio-33bd2293f34c
7. https://medium.com/@britt.barak/from-view-to-pixel-5a9b7470f3fd
8. https://medium.com/@britt.barak/rendering-phase-by-phase-7ea8c9885eb2
9. https://medium.com/@britt.barak/measure-layout-draw-483c6a4d2fab
10. https://medium.com/@britt.barak/layout-once-layout-twice-sold-aef156ff16a4
11. https://medium.com/@britt.barak/to-constraint-or-not-to-constraint-8030e607a2aa
