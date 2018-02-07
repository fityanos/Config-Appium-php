# Configure Appium
### includes everything as a new machine
1. Install Homebrew: /usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"

2. Install PHP and Composer OR related programing language

3. Install Node JS and NPM

4. Install JAVA and JDK

5. Install Android studio and make sure it in Applications

4. Install Appium server GLOBALLY through npm | npm install -g appium

5. Install Appium Desktop for Inspecting the Elements.

6. Install appium-doctor | npm install appium-doctor


# How to set ANDROID_HOME and JAVA_HOME
   `   

       1. ANDROID_HOME => Android studio you download as it contains sdk in it (open new project and then you will get message to install dependencies such as sdk)
       2. cd Library/Android/sdk
       
       3. THEN pwd (to get the path) 
       
       4. JAVA_HOME => export JAVA_HOME=/Library/Java/JavaVirtualMachines/jdk1.8.0_65.jdk/Contents/Home
       
       5. export ANDROID_HOME=/Users/anasfitiani/Library/Android/sdk/
       
       6. export PATH=${PATH}:$ANDROID_HOME/tools:$ANDROID_HOME/platform-tools:$ANDROID_HOME/build-tools
       
       7. export PATH=$PATH:/usr/local/share/npm/bin/
       
       8. PATH=${JAVA_HOME}/bin:$PATH  
       
       9. Save`
   
   
   ### When you run appuim-doctor --android you will get:
   
       
       info AppiumDoctor Appium Doctor v.1.4.3
       
       info AppiumDoctor ### Diagnostic starting ###
       
       info AppiumDoctor  ✔ The Node.js binary was found at: /Users/anasfitiani/.nvm/versions/node/v6.2.2/bin/node
       
       info AppiumDoctor  ✔ Node version is 6.2.2
       
       info AppiumDoctor  ✔ ANDROID_HOME is set to: /Users/anasfitiani/Library/Android/sdk/
       
       info AppiumDoctor  ✔ JAVA_HOME is set to: /Library/Java/JavaVirtualMachines/jdk1.8.0_65.jdk/Contents/Home
       
       info AppiumDoctor  ✔ adb exists at: /Users/anasfitiani/Library/Android/sdk/platform-tools/adb
       
       info AppiumDoctor  ✔ android exists at: /Users/anasfitiani/Library/Android/sdk/tools/android
       
       info AppiumDoctor  ✔ emulator exists at: /Users/anasfitiani/Library/Android/sdk/tools/emulator
       
       info AppiumDoctor  ✔ Bin directory of $JAVA_HOME is set
       
       info AppiumDoctor ### Diagnostic completed, no fix needed. ###
       
       info AppiumDoctor
       
       info AppiumDoctor Everything looks good, bye!
       
       info AppiumDoctor`
   
   
   ### When you run appuim-doctor --ios you will get:
      
      info AppiumDoctor ### Diagnostic starting ###
      
      info AppiumDoctor  ✔ The Node.js binary was found at: /Users/anasfitiani/.nvm/versions/node/v6.2.2/bin/node
      
      info AppiumDoctor  ✔ Node version is 6.2.2
      
      info AppiumDoctor  ✔ Xcode is installed at: /Applications/Xcode.app/Contents/Developer
      
      info AppiumDoctor  ✔ Xcode Command Line Tools are installed.
      
      info AppiumDoctor  ✔ DevToolsSecurity is enabled.
      
      info AppiumDoctor  ✔ The Authorization DB is set up properly.
      
      info AppiumDoctor  ✔ Carthage was found at: /usr/local/bin/carthage
      
      info AppiumDoctor  ✔ HOME is set to: /Users/anasfitiani
      
      info AppiumDoctor ### Diagnostic completed, no fix needed. ###
      
      info AppiumDoctor
      
      info AppiumDoctor Everything looks good, bye!`
   
   
   
   
   ### Now, how to set or export your paths such as android home or java home:
   `
       
       1. run nano ~/.bash_profile
       2. add:
       
          a. export JAVA_HOME=/Library/Java/JavaVirtualMachines/jdk1.8.0_65.jdk/Contents/Home
       
          b. export ANDROID_HOME=/Users/anasfitiani/Library/Android/sdk/
          
          c. export PATH=${PATH}:$ANDROID_HOME/tools:$ANDROID_HOME/platform-tools:$ANDROID_HOME/build-tools
          
          d. export PATH=$PATH:/usr/local/share/npm/bin/
          
          e. PATH=${JAVA_HOME}/bin:$PATH
          
       3. save
       4. close the terminal and re open it
       5. source ~/.bash_profile
       6. run appium-doctor`
      
      
      
   ### Configure Appium desktop and define desire capabilities:
      
   `
         
       1. Server: 0.0.0.0  
       2. Port: 4723 || 4725
          
       3. desire capabilities Android:
          {
            "platformName": "Android",
            
            "automationName": "Appium",
            
            "deviceName": "Android device",
            
            "appPackage": "com.tajawal",
            
            "appActivity": "com.tajawal.splash.SplashActivity",
            
            "noReset": false
          }
          
       4. Save desire capabilities`
      