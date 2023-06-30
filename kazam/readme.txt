[How to install "Kazam" and update its translation of your installed application]

Download ja.mo and then overwrite the existing app's .mo file with this Japanese .mo file from the commandline as below:


[Example]

root@mx1:/home/demo/# apt install kazam

root@mx1:/home/demo/# cp ja.mo /usr/share/locale/ja/LC_MESSAGES/kazam.mo

Note: "ja" is a locale code for Japanese language. 

END.
