# Configure Appium with PHP


#### Installation and Setup as a New Machine:
    1. Install PHP and Composer
    
    2. Install latest codeCeption

    3. Install Node JS and npm

    4. Install JAVA and JDK

    5. Install Android studio and make sure it in Applications

    6. Install Appium server GLOBALLY through npm | npm install -g appium

    7. Install Appium Desktop for Inspecting the Elements

    8. Run npm install appium-doctor to install appium-doctor


 - **_ANDROID_** :octocat: 

#### Now, how to set or export your paths such as ANDROID_HOME || JAVA_HOME:
   
    1. run nano ~/.bash_profile
    2. add:
    
       a. export JAVA_HOME=/Library/Java/JavaVirtualMachines/jdk1.8.0_65.jdk/Contents/Home
       
       b. export ANDROID_HOME=/Users/usr/Library/Android/sdk/
          
       c. export PATH=${PATH}:$ANDROID_HOME/tools:$ANDROID_HOME/platform-tools:$ANDROID_HOME/build-tools
          
       d. export PATH=$PATH:/usr/local/share/npm/bin/
          
       e. PATH=${JAVA_HOME}/bin:$PATH
          
    3. save
    4. Relaunch terminal session
    5. source ~/.bash_profile
    6. run appium-doctor


#### How to set Android dependencies:  

       1. ANDROID_HOME => Android studio you download as it contains sdk in it (open new project and then you will get message to install dependencies such as sdk)
       
       2. cd Library/Android/sdk (or your respictive path)
       
       3. execute pwd (to get the path while you are in the dir) 
       
       4. JAVA_HOME => export JAVA_HOME=/Library/Java/JavaVirtualMachines/jdk1.8.0_65.jdk/Contents/Home
       
       5. export ANDROID_HOME=/Users/usr/Library/Android/sdk/
       
       6. export PATH=${PATH}:$ANDROID_HOME/tools:$ANDROID_HOME/platform-tools:$ANDROID_HOME/build-tools
       
       7. export PATH=$PATH:/usr/local/share/npm/bin/
       
       8. PATH=${JAVA_HOME}/bin:$PATH  
       
       9. Save
   
   
#### When you run appuim-doctor --android you will get:
   
       info AppiumDoctor Appium Doctor v.1.4.3
       
       info AppiumDoctor ### Diagnostic starting ###
       
       info AppiumDoctor  ✔ The Node.js binary was found at: /Users/usr/.nvm/versions/node/v6.2.2/bin/node
       
       info AppiumDoctor  ✔ Node version is 6.2.2
       
       info AppiumDoctor  ✔ ANDROID_HOME is set to: /Users/usr/Library/Android/sdk/
       
       info AppiumDoctor  ✔ JAVA_HOME is set to: /Library/Java/JavaVirtualMachines/jdk1.8.0_65.jdk/Contents/Home
       
       info AppiumDoctor  ✔ adb exists at: /Users/usr/Library/Android/sdk/platform-tools/adb
       
       info AppiumDoctor  ✔ android exists at: /Users/usr/Library/Android/sdk/tools/android
       
       info AppiumDoctor  ✔ emulator exists at: /Users/usr/Library/Android/sdk/tools/emulator
       
       info AppiumDoctor  ✔ Bin directory of $JAVA_HOME is set
       
       info AppiumDoctor ### Diagnostic completed, no fix needed. ###
       
       info AppiumDoctor
       
       info AppiumDoctor Everything looks good, bye!
       
       info AppiumDoctor
       
       
##### If you faced erro such as "Error: listen EADDRINUSE 0.0.0.0:4723" on CLI or Appium GUI try to change the Appium port to 4727

##### Make sure to tap on the mobile device to do more than just charging the device

       
       
#### Configure Appium desktop and define desire capabilities for ANDROID:
               
              1. Server: 0.0.0.0  
              2. Port: 4723
                 
              3. desire capabilities Android:
                 {
                   "platformName": "Android",
                   
                   "automationName": "Appium",
                   
                   "deviceName": "Android device",
                   
                   "appPackage": "related_app_package",
                   
                   "appActivity": "related_app_activity",
                   
                   "noReset": false
                 }
                 
              4. Save desire capabilities
              
              
              
              
    
    
    
              
              
   - **_IOS_** :octocat: 
   
#### When you run appuim-doctor --ios you will get:
      
      info AppiumDoctor ### Diagnostic starting ###
      
      info AppiumDoctor  ✔ The Node.js binary was found at: /Users/usr/.nvm/versions/node/v6.2.2/bin/node
      
      info AppiumDoctor  ✔ Node version is 6.2.2
      
      info AppiumDoctor  ✔ Xcode is installed at: /Applications/Xcode.app/Contents/Developer
      
      info AppiumDoctor  ✔ Xcode Command Line Tools are installed.
      
      info AppiumDoctor  ✔ DevToolsSecurity is enabled.
      
      info AppiumDoctor  ✔ The Authorization DB is set up properly.
      
      info AppiumDoctor  ✔ Carthage was found at: /usr/local/bin/carthage
      
      info AppiumDoctor  ✔ HOME is set to: /Users/usr
      
      info AppiumDoctor ### Diagnostic completed, no fix needed. ###
      
      info AppiumDoctor
      
      info AppiumDoctor Everything looks good, bye!
   
   
   
#### Configure Appium desktop and define desire capabilities for IOS Simulator:
                  
                 1. Server: 0.0.0.0  
                 2. Port: 4723
                    
                 3. desire capabilities iOS:
                    {
                      "app": "path_to_your_application_.ipa_file",
                      
                      "platformName": "iOS",
                      
                      "platformVersion": "iOS_Version Example (10.1)",
                      
                      "deviceName": "iPhone Simulator",
                      
                      "automationName": "XCUITest"
                    }
                    
                 4. Save desire capabilities
                 
                 
                 
#### Configure Appium desktop and define desire capabilities for IOS Real device:
                     
                    1. Server: 0.0.0.0  
                    2. Port: 4723
                       
                    3. desire capabilities iOS:
                       {
                         "app": "path_to_your_application_.ipa_file",
                         
                         "platformName": "iOS",
                         
                         "deviceName": "your_iphone_device_name",
                         
                         "xcodeOrgId": "developement_team_id from developement (Apple developer team identifier string)",
                         
                         "xcodeSigningId": "iPhone Developer (string representing a signing certificate. iPhone Developer by default)",
                         
                         "udid": "the ID((Unique Device Identifier) of real device that can be retrieved by running 'instruments -s devices' while device is connected)",
                         
                         "platformVersion": "Ex 11.1",
                         
                         "useNewWDA": true,
                         
                         "fullReset": true
                       }
                       
                    4. Save desire capabilities              
   
      
      
      

      