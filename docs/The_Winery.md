##Ingredients (components)
The below components make this tool functional. This repository is powered by:
### Composer

	curl http://getcomposer.org/installer | php
	php composer.phar install

Or you may need to just update to install thhe dependancies listed in `composer.json` via:

	php composer.phar update
	

### Pear

	wget http://pear.php.net/go-pear.phar
	php go-pear.phar

### PHPUnit 3.x & Up

	pear channel-discover pear.phpunit.de
	pear channel-discover components.ez.no
	pear channel-discover pear.symfony-project.com
	pear install phpunit/PHPUnit
	
##Getting tipsy (local setup)

## Mac OS X
Make sure you have `Safari`, `Internet Explorer`, `Chrome` & `Firefox` downloaded on the machines used for testing, respectively.

Open Terminal, then navigate to the project directory:

	cd ~/path/to/saucey/

### Firefox
By default Selenium starts with default:

	java -jar vendor/saucey/drivers/selenium-server-standalone-2.45.0.jar
	
Open a new window/tab, then:

	vendor/bin/behat
	
### Chrome
In `behat.yml`, from the root of the project directory.

    selenium2:
      browser: chrome

Start Selenium with the chromeDriver as a parameter:

	java -jar vendor/saucey/drivers/selenium-server-standalone-2.45.0.jar -Dwebdriver.chrome.driver=vendor/saucey/drivers/chromedriver

Open a new window/tab, then: 

	vendor/bin/behat
	
### Safari
In `behat.yml`, from the root of the project directory.

    selenium2:
      browser: safari

####Requirements
1. Download this [plugin](https://github.com/SeleniumHQ/selenium/raw/master/javascript/safari-driver/prebuilt/SafariDriver.safariextz).
2. Install the [developers certificate](https://developer.apple.com/account/overview.action) in your "Keychain"
3. Open Safari
4. Go to Preferences
5. Click on the Extensions tab
6. Make sure WebDriver for WebDriver 2.38.0 is checked "enabled"
7. Close Safari

Start Selenium with the safariDriver as a parameter:

	java -jar vendor/saucey/drivers/selenium-server-standalone-2.45.0.jar -Dwebdriver.safari.noinstall=true
	
Open a new window/tab, then: 

	vendor/bin/behat

	
## Windows
### Requirements
If you're on a Virtual Machine, there are a couple of things needed to get behat running. Make sure you have `Internet Explorer`, `Chrome` & `Firefox` downloaded on your machine or virtual machine. 

1. [Visual C++ 2008 Redistributables](http://www.microsoft.com/downloads/details.aspx?familyid=9B2DA534-3E03-4391-8A4D-074B9F2BC1BF)
2. [WAMP](http://www.wampserver.com/en/)
3. Add java to your PATH via [steps](https://www.java.com/en/download/help/path.xml)
4. Similar to the above step, add PHP to your PATH `C:\wamp\bin\php\php5.5.12;`
5. Depending on your Internet Explorer settings, you may need to [Enable Protection Mode](http://stackoverflow.com/questions/14952348/not-able-to-launch-ie-browser-using-selenium2-webdriver-with-java)


Open Command Prompt, then navigate to the project directory:

	cd path\to\saucey
	
### Internet Explorer
Start Selenium with the ieDriver as a parameter:

	java -jar vendor\saucey\drivers\selenium-server-standalone-2.45.0.jar -Dwebdriver.ie.driver=vendors\saucey\drivers\IEDriverServer.exe

Open a new window/tab, then: 

	vendor\bin\behat
		
### Firefox 
In `behat.yml`, from the root of the project directory.

Then change:

    selenium2:
      browser: ie

To:

    selenium2:
      browser: firefox
 
Start Selenium:

	java -jar vendor\saucey\drivers\selenium-server-standalone-2.45.0.jar
  
Open a new window/tab, then: 

	vendor\bin\behat
	
###Chrome
In `behat.yml`, from the root of the project directory.

Then change:

    selenium2:
      browser: ie

To:

    selenium2:
      browser: chrome
 
Start Selenium with the firefoxDriver (default) as a parameter:

	java -jar vendor\saucey\drivers/\elenium-server-standalone-2.45.0.jar -Dwebdriver.chrome.driver=vendors\saucey\drivers\chromedriver.exe
  
Open a new window/tab, then: 

	vendor\bin\behat
		
#Getting drunk (cloud setup)
Find additional information on drivers [here](https://saucelabs.com/platforms/webdriver).

To point **saucey** to SauceLabs, you'd need your `user_name` and `access_key`. 

After registering for a **free** [SauceLabs](https://saucelabs.com/) account:

1. Get your username and api-key, *should be available via /account.* Copy the info into your clipboard.
2. Open the `behat.yml` file with your favorite IDE and replace all instances of `username:api-key` with your username (used to log in) and api-key. Save.
3. To test something on a localhost in the cloud, you can open a tunnel with sauce connect. With your username and api-key/access_key from the steps above, run:

		vendor/bin/sauce_config user_name access_key

	To start the connect tunnel:

		vendor/sauce/connect/bin/sauce_connect 


## Mac OS X Simulating
### Firefox
In `behat.yml`, from the root of the project directory.

	selenium2:
	  browser: firefox
	  wd_host: user_name:access_key@ondemand.saucelabs.com/wd/hub
	  capabilities: {  "platform": "OS X 10.8", "version": "8", "name": "NAME THIS SUITE"}

Then: 

	vendor/bin/behat
	
### Chrome
In `behat.yml`, from the root of the project directory.

	selenium2:
	  browser: chrome
	  wd_host: user_name:access_key@ondemand.saucelabs.com/wd/hub
	  capabilities: {  "platform": "OS X 10.8", "version": "8", "name": "NAME THIS SUITE"}

Then: 

	vendor/bin/behat
	
### Safari
In Terminal or Finder open `behat.yml` in the root of the project directory.

	selenium2:
	  browser: safari
	  wd_host: user_name:access_key@ondemand.saucelabs.com/wd/hub
	  capabilities: {  "platform": "OS X 10.8", "version": "8", "name": "NAME THIS SUITE"}

Then: 

	vendor/bin/behat
	
##Windows Simulating
### Internet Explorer
In `behat.yml`, from the root of the project directory.

	selenium2:
	  browser: ie
	  wd_host: user_name:access_key@ondemand.saucelabs.com/wd/hub
	  capabilities: {  "platform": "Windows 7", "version": "8", "name": "NAME THIS SUITE"}
	  
Then: 

	vendor/bin/behat
	
### Firefox
In `behat.yml`, from the root of the project directory.

	selenium2:
	  browser: firefox
	  wd_host: user_name:access_key@ondemand.saucelabs.com/wd/hub
	  capabilities: {  "platform": "Windows 2012", "version": "10", "name": "NAME THIS SUITE"}
	  
Then: 

	vendor/bin/behat

### Chrome
In `behat.yml`, from the root of the project directory.

	selenium2:
	  browser: chrome
	  wd_host: user_name:access_key@ondemand.saucelabs.com/wd/hub
	  capabilities: {  "platform": "Windows 7", "version": "39", "name": "NAME THIS SUITE"}
	  
Then: 

	vendor/bin/behat

## Cloud Mobile Automated Testing
## iPad
In `behat.yml`, from the root of the project directory.

      selenium2:
        browser: iPad
	    wd_host: user_name:access_key@ondemand.saucelabs.com/wd/hub
        capabilities: {  "platform": "OS X 10.9", "version": "8.1", "name": "NAME THIS SUITE"}
	  
Additionally, you can add `"deviceOrientation": "landscape",` or `portrait` to test orientation. 

Then: 

	vendor/bin/behat

## iPhone
In `behat.yml`, from the root of the project directory.

      selenium2:
        browser: iPhone
	    wd_host: user_name:access_key@ondemand.saucelabs.com/wd/hub
        capabilities: {  "platform": "OS X 10.9", "version": "8.1", "name": "NAME THIS SUITE"}

Then: 

	vendor/bin/behat

## Android Phone
In `behat.yml`, from the root of the project directory.

      selenium2:
        browser: android
	    wd_host: user_name:access_key@ondemand.saucelabs.com/wd/hub
        capabilities: {  "platform": "Linux", "version": "4.4", "name": "NAME THIS SUITE", "deviceType": "phone"}
	  
Then: 

	vendor/bin/behat

## Android Tablet
In `behat.yml`, from the root of the project directory.

      selenium2:
        browser: android
	    wd_host: user_name:access_key@ondemand.saucelabs.com/wd/hub
        capabilities: {  "platform": "Linux", "version": "4.4", "name": "NAME THIS SUITE", "deviceType": "tablet"}
	  
Additionally, you can add `"deviceOrientation": "landscape",` or `portrait` to test orientation. 


Then: 

	vendor/bin/behat
