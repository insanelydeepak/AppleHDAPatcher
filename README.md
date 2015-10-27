![alt text](http://i58.tinypic.com/wjb9j4.png)

##  AppleHDAPatcher - v1.1 - El Capitan Supported. ###

### Please do not upload it on other servers ###.
 
Drag a codec folder (or various) to the app.

### Each codec folder must contain: ###
 
	•	Platforms.xml.zlib
	•	layout*.xml.zlib
	•	hdaconfig.txt
	•	binpatch.txt (optional)
	•	README* (optional)

The file hdaconfig.txt must contain the entries to be inserted into Info.plist of AppleHDAHardwareConfigDriver. 
To create this file just copy the relevant parts to the clipboard (Command+C) and run in terminal:

```
pbpaste | pl > ~/Desktop/hdaconfig.txt

```

Sample of what must be copied to clipboard:

```

<dict>
   <key>AFGLowPowerState</key>
   <data>
   AwAAAA==
   </data>
   <key>CodecID</key>
   <integer>283904135</integer>
   <key>ConfigData</key>
   <data>
   AUccEAFHHUABRx4RAUcfAQFXHCABVx0QAVce
   AQFXHwEBZxwwAWcdYAFnHgEBZx8BAXccQAF3
   HSABdx4BAXcfAQGHHFABhx2QAYceoAGHH5AB
   lxxgAZcdkAGXHoEBlx8CAacccAGnHTABpx6B
   AacfAQG3HIABtx1AAbceIQG3HwEB5xyQAecd
   4AHnHkUB5x8B
  </data>
  <key>FuncGroup</key>
  <integer>1</integer>
  <key>LayoutID</key>
  <integer>4</integer>
</dict>

```
Sample file generated by the command:

```
{
    AFGLowPowerState = <03000000>;
    CodecID = 283904135;
    ConfigData = <01471c10 01471d40 01471e11 01471f01 01571c20 01571d10 01571e01 01571f01 01671c30 01671d60 01671e01 01671f01 01771c40 01771d20 01771e01 01771f01 01871c50 01871d90 01871ea0 01871f90 01971c60 01971d90 01971e81 01971f02 01a71c70 01a71d30 01a71e81 01a71f01 01b71c80 01b71d40 01b71e21 01b71f01 01e71c90 01e71de0 01e71e45 01e71f01>;
    FuncGroup = 1;
    LayoutID =  7;
}

```
The file binpatch.txt must contain the binpatch bytes sequence (if needed), for instance:
```
10ec0887
```
In AppleHDAPatcher.app/Contents/Resources there must be an updated original AppleHDA.

Credits:
 
Binpatch script by ###bcc9###
The ###oldnapalm#### for all the help with the script.