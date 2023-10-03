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

Two categories of flutter widgets
,,
- visible (output and input)
- invisible (layout and control)

# History

in ==2015==, Google unveiled Flutter

in ==2017==, an alpha version of it (0.0.6) was released to the public for the first time.

in ==December 2018==, Flutter 1.0 was released

has a portable runtime for high-quality mobile apps and primarily based on the C++ language ;; flutter engine

the flutter engine takes google's open-source graphics library, ==Skia== to render low-level graphics

# StatefulWidget

A `StatefulWidget` has state ==information==

`StatefulWidget` widgets are dynamic because it can change the inner data during the ==widget lifetime==

This widget does not have a ==`build()`== method

this widget has the ==`createState()`== method, which returns a class that extends the ==flutters state class==

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