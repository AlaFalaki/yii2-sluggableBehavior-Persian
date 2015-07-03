## yii2-sluggableBehavior-Persian
a snippet to help persian users, to create persian slugs in Yii2

###What is the problem?
If you are from Iran, and want to make SluggableBehavior work for your Yii2 project, you certainly saw that Yii2 does not recognize Farsi, if you type "مطلب اول" in the title, SluggableBehavior will generate "matlb-awl".

###Why this problem happens?
Yii2 uses the intl php extension (transliterate), and since this extension (as far as i know) does not support Farsi, it tries to translate it to something close to what it think the phrase is!
> (if i'm wrong and there is a better way to make intl extension understand Farsi, I'll be glad to hear it)

###How to fix it?
