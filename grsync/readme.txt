[How to update translation of your installed application]

Overwrite the existing app's .mo file with updated .mo file from the commandline as below:


[Example]
root@mx1:/home/demo/# cp ja.mo /usr/share/locale/ja/LC_MESSAGES/mate-utils.mo
or
root@mx1:/home/demo/# cp ja_JP.mo /usr/share/locale/ja/LC_MESSAGES/mate-utils.mo

Note: "ja" or "ja_JP" is a locale code for Japanese language. 

END.
