# android-auto-generate-dimension

## Find your support screen size here:

        http://dpi.lv/
        https://design.google.com/devices/

## Structure:
#### 1. Auto create dimension values with defined values:

        createDimen {    
            fromDimen = 360
            positiveMaxDP = 200//change to 600 or any other value if needed
            positiveMaxSP = 60//change to 600 or any other value if needed
            negativeMaxDP = 60//change to 600 or any other value if needed
            negativeMaxSP = 20//change to 600 or any other value if needed
            type = DimenType.AUTO_CREATE
        }

#### 2. Auto get and make dimension file with value from your res/layout:   
    
        createDimen {
            fromDimen = 360
            positiveMaxDP = 200//change to 600 or any other value if needed
            positiveMaxSP = 60//change to 600 or any other value if needed
            negativeMaxDP = 60//change to 600 or any other value if needed
            negativeMaxSP = 20//change to 600 or any other value if needed
            type = DimenType.FROM_LAYOUT
        }
        

#### 3. Auto generate dimension values from your defined dimension file for
other screen size:
  
        createDimen {
            fromDimen = 360
            positiveMaxDP = 200//change to 600 or any other value if needed
            positiveMaxSP = 60//change to 600 or any other value if needed
            negativeMaxDP = 60//change to 600 or any other value if needed
            negativeMaxSP = 20//change to 600 or any other value if needed
            type = DimenType.FROM_DIMEN_FILE
            dimenFileName = 'values/dimens.xml' // name of file, for type = DimenType.FROM_DIMEN_FILE only
        }

## Use:

        Copy file autodimension.gradlew to root of your project. If you use eclispe please install gradle
        then build this project to generate file dimension then add as library project
    
In terminal of android studio execute the following command:

    **./gradlew createDimen**
    
If build success you can see many value-sw directories are created with 
    dimensions values.
    
If your project has many modules, add:

    **apply from '../autodimension.gradle'**
into your gradle file of module
and using command: 

    **./gradlew :{module_name}:createDimen**
to generate dimension files.

After generate you have:

        src/main/res/

        values-sw360dp
        values-sw390dp
        values-sw420dp
        values-sw450dp
        values-sw480dp
        values-sw510dp
        values-sw540dp
        values-sw570dp
        values-sw600dp
        values-sw630dp
        values-sw660dp
        values-sw690dp
        values-sw720dp
        values-sw750dp
        values-sw780dp
        values-sw810dp
## Note:
        With size of actionbar, you must create different sizes, not using this tool (you can see the different size of tablet and phone)

## Contact:

    If you have any problem, please contact me: manhduongvtt@gmail.com
    
    
