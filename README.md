# Configure Appium with codeception
###How to set up Appium with codeception
### includes everything as a new machine

1. Install Homebrew: /usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"
2. Install PHP and Composer
3. Install Node JS and NPM
4. Install JAVA and JDK
5. Install Android studio and make sure it in Applications
4. Install Appium server GLOBALLY through npm | npm install -g appium
5. Install Appium Desktop for Inspecting the Elements.
6. Install appium-doctor | npm install appium-doctor


# How to set ANDROID_HOME && JAVA_HOME

   ANDROID_HOME => Android studio you download as it contains sdk in it
   cd Library/Android/sdk
   THEN
   pwd (to get the path) 
   
   JAVA_HOME =>     
   export JAVA_HOME=/Library/Java/JavaVirtualMachines/jdk1.8.0_65.jdk/Contents/Home
   export ANDROID_HOME=/Users/anasfitiani/Library/Android/sdk/
   export PATH=${PATH}:$ANDROID_HOME/tools:$ANDROID_HOME/platform-tools:$ANDROID_HOME/build-tools
   export PATH=$PATH:/usr/local/share/npm/bin/
   PATH=${JAVA_HOME}/bin:$PATH  
   
   ###AND SAVE
   
   
   ###WHEN YOU RUN appuim-doctor --android you will get
   ➜  qa git:(WQA-260) appium-doctor --android
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
   info AppiumDoctor
   
   
   ###WHEN YOU RUN appuim-doctor --ios you will get:
   ➜  qa git:(WQA-260) appium-doctor --ios
   info AppiumDoctor Appium Doctor v.1.4.3
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
   info AppiumDoctor Everything looks good, bye!
   
   
   ### NOW, how to set or export your paths such as android home or java home:
   1. run nano ~/.bash_profile
   2. add:
   export JAVA_HOME=/Library/Java/JavaVirtualMachines/jdk1.8.0_65.jdk/Contents/Home
      export ANDROID_HOME=/Users/anasfitiani/Library/Android/sdk/
      export PATH=${PATH}:$ANDROID_HOME/tools:$ANDROID_HOME/platform-tools:$ANDROID_HOME/build-tools
      export PATH=$PATH:/usr/local/share/npm/bin/
      PATH=${JAVA_HOME}/bin:$PATH
      3. save
      4. close the terminal and re open it
      5. source ~/.bash_profile
      6. run appium-doctor
      