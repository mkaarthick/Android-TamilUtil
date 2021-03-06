﻿Android-TamilUtil
=================

This library can be used to convert Unicode string to Bamini, Anjal, TAB, TAM and TSCII.

Steps to use this library.

1. Download the library
2. Import the library into Eclipse as new Project
3. Add the library to your project as library (Right click -> Project -> Android -> Click "Add" button and select this library.)

This is a sample on how you can utilise the library

    // Initialise the Typeface (assumes TSCII, Bamini, Anjal, TAB or TAM font located inside assets/fonts folder)
    Typeface tf = Typeface.createFromAsset(getAssets(),"fonts/mylai.ttf");
    // Initialises the TextView
    TextView tv = (TextView)findViewById(R.id.textView1);
    //Setting the Typeface
    tv.setTypeface(tf);
    //Magic happens here ;) encoding conversion
    String TSCIIString = TamilUtil.convertToTamil(TamilUtil.TSCII, "வணக்கம் அன்ரொயிட்");
    //Setting the new string to TextView
    tv.setText(TSCIIString);

Final out put would look something like below

![Screen Shot Tamil Unicode Converter Utill](https://raw.github.com/mayooresan/Android-TamilUtil/master/ScreenShot.png "Android Tamil")

Inspired by [Tamil Visai](https://github.com/thamizha/android-tamilvisai) and [Pongu thamizh by Suratha](http://www.suratha.com/reader.htm). 

Special thanks to [Mauran](http://mauran.blogspot.com/) for sharing the conversion code for TAB, TAM and Anjal
