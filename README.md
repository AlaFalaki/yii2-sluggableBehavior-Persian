## Yii2 sluggableBehavior Persian
a snippet to help persian users, to create persian slugs in Yii2
(If you don't know what the SluggableBehavior is, read [this tutorial](http://code.tutsplus.com/tutorials/programming-with-yii2-sluggable-behavior--cms-23222) or go away :)

###What is the problem?
If you are from Iran, and want to make SluggableBehavior work for your Yii2 project, you certainly saw that Yii2 does not recognize Farsi, if you type "مطلب اول" in the title, SluggableBehavior will generate "matlb-awl".

###Why this problem happens?
Yii2 uses the intl php extension (transliterate), and since this extension (as far as i know) does not support Farsi, it tries to translate it to something close to what it think the phrase is!
> (if i'm wrong and there is a better way to make intl extension understand Farsi, I'll be glad to hear it)

###How to fix it?
Well, if you trace the SluggableBehavior.php (path/to/yii/vendor/yiisoft/yii2/behaviors/SluggableBehavior.php), you found out that it usess inflector helper (path/to/yii/vendor/yiisoft/yii2/helpers/BaseInflector.php) to generate slugs, if you comment out line 425 and make slightly change to linke 426 in BaseInflector.php it should works.

**Simply, you can replace the BaseInflector.php file that i uploaded here, with the file in the framework core.**
>I don't know if this is the best practice to make the sluggableBehavior work for Farsi, but it works for me for now, if i find anything better, i'll let you know.


[My Website](http://AlaFalaki.ir)

[My Twitter](http://twitter.com/AlaFalaki)
