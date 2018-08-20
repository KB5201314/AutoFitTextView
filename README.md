MODIFYED（fork） VERSION
================

- 增加了对maxHeight属性值的参考
- 除去对末尾字符的限定以修复中文支持
- 修改限定方式为maxHeight和maxLines两种，优先判断maxLines是否设置，避免了只设置maxLines时发生的一些奇奇怪怪的问题，例如反复设置同一段文本的过程中，文字越来越大最后才趋于正常


[![Release](https://img.shields.io/github/release/AndroidDeveloperLB/AutoFitTextView.svg?style=flat)](https://jitpack.io/#AndroidDeveloperLB/AutoFitTextView)

AutoFitTextView
===============

A TextView that automatically fit its font and line count based on its available size and content

This code is heavily based on [**this StackOverflow thread**][1].

The sample shows how the library can handle various parameters being changed on the TextView: width, height, number of lines allowed, and the content (text) itself. You can play with the various properties to see how the library handle them.

Note that even though the sample is of API 16, it should work fine on most cases for much older versions.

A nice example of how to use an EditText that has this functionality can be found [here][4] (didn't test it, but it looks promising).

Preview
--
![preview animation][2]

Import using Gradle
--

	allprojects {
		repositories {
			...
			maven { url "https://jitpack.io" }
		}
	}
	
		dependencies {
	        compile 'com.github.AndroidDeveloperLB:AutoFitTextView:XXX'
	}

You can find recent version here (replace XXX):

https://jitpack.io/#AndroidDeveloperLB/AutoFitTextView

Known issues
------------

 - API 12-15 (including) of Android might have issues as a cause of [**this known bug**][3], but in most cases it should work fine there too. 
 


  [1]: http://stackoverflow.com/questions/16017165/auto-fit-textview-for-android/21851239
  [2]: https://raw.githubusercontent.com/AndroidDeveloperLB/AutoFitTextView/master/animationPreview.gif
  [3]: https://code.google.com/p/android/issues/detail?id=22493
  [4]: https://viksaaskool.wordpress.com/2014/11/16/using-auto-resize-to-fit-edittext-in-android/
