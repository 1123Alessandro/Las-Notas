---
tags: fc, appdev
course: 26011 App Development
---

open-source UI software development kit created by Google ;; flutter

flutter is an ==SDK== that is used to build high performance, modern, and beautiful apps with ease.

flutter is used to develop ==applications== for Android, iOS, Windows, Mac, Linux, Google Fuchsia and the web

flutter uses the ==Dart== programming language

flutter ==natively compiles== applications for mobile, web, and desktop from a single ==codebase==

flutter is optimized for ==2D mobile apps== that want to run on both Android and iOS

Flutter is Engineered for high development velocity apps in which ==Stateful Hot Reload== allows user to change their code and see it come to life in less than a second without losing the state of that app

Injecting updated source code files into the running Dart VM ;; Hot reload

Flutter uses neither ==WebView nor the OEM== widgets that shipped with the device. Instead, Flutter uses its own high-performance rendering engine to draw widgets

==Dart== is a general-purpose programming language originally developed by google and later approved as a standard by ==Ecma (ECMA-408)==

describes how your app view hsould look like with their current configuration and state ;; widget

When you made any alteration in the code, the widget rebuilds its description by ==calculating the difference== of previous and current widget to determine the minimal changes for rendering in Ul of the app

A widget is either stateful or stateless. If a widget can change when a user ==interacts with it==

# Visible and Invisible Widgets 
Two categories of flutter widgets
,,
- visible (output and input)
- invisible (layout and control)
"
The ==visible widgets== are related to the user input and output data.

## Important tpyes of visible widgets
This holds some text to display on the screen ;; Text 

This widget holds the image which can fetch it from multiple sources like form the asset folder or directly from the URL ;; image 

### Image Constructors 

==Image== : It is a generic image loader, which is used by Image Provider
==asset== : Loads the image from your project ==asset== folder
==file== : it loads image from the system folder
==memory== : Loads the image from the memory
==network== : It loads images from the internet 

This widget acts as a container for stroing the Icon in Flutter ;; Icon

==Invisible widgets== are related to hte layout and control of widgets. It provides controlling how the widgets actually behave and how they will look onto the screen.

### Important tpyes of Invisible widgets 

It is a type of widget that arranges all its children's widgets in a vertical alignment.  ;; Column

The ==row== widget is similar to the column widget, but it constructs a widget horizontally rather than vertically 

this widget provides a framework that allows you to add common material design elements like AppBar, Floating Action Buttons, Drawers, etc ;; Scaffold

It is an essential widget, which is mainly used for overlapping a widget, such as a button on a background gradient.  ;; Stack

# History

in ==2015==, Google unveiled Flutter

in ==2017==, an alpha version of it (0.0.6) was released to the public for the first time.

in ==December 2018==, Flutter 1.0 was released

has a portable runtime for high-quality mobile apps and primarily based on the C++ language ;; flutter engine

It implements ==Flutter core libraries== that include animation, and grpahics, fiole and network I/O, plugin architecture, accessibility support, and a dart runtime for developing, compiling and running Flutter applications

the flutter engine takes google's open-source graphics library, ==Skia== to render low-level graphics

# StatefulWidget and Stateless widgets 

A `StatefulWidget` has state ==information==

`StatefulWidget` widgets are dynamic because it can change the inner data during the ==widget lifetime==

This widget does not have a ==`build()`== method

this widget has the ==`createState()`== method, which returns a class that extends the ==flutters state class==

==Stateful Widget== can build in many different BuildContexts

==Stateless Widget== creattes a new State object for each BuildContext 

A widget that never changes ;; stateless widget

Examples of Stateful Widgetes 
"
- Checkbox
- Radio button
- TextField
"

Examples of Stateless Widget
"
- text
- Icon
- Icon Button
- Raised button
"

==Stateful Widget== Override the CreateState and return State

==Stateless Widget== Override the build() and return Widget

==Stateful Widget== is used when the user want to change the UI dynamically 

==Stateless Widget== is used when the UI remains constant during runtime 

In ==Stateful widgets== when the state changes, the state object calls ==setState()==, telling the framework to redraw the widget

# Flutter Architecture

Framework
,,
- Dart
	- material
	- cupertino
	- widgets
	- rendering
	- animation
	- painting
	- gestures
	- foundation

Engine
,,
- C++
- Skia
- Dart
- Platform Ch.

Platform
,,
- Android Shell
- iOS Shell
- Embedder API

