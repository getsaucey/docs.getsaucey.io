#Pour a glass (Init & Install)
To make things simpler, we'll use [Robo](https://github.com/Codegyre/Robo) for all of our task management needs. Lets install it! Install all dependancies through composer, if you run in to any issues please see the [wiki](https://github.com/withpulp/saucey/wiki/). 

For all instances of `<tag>` replace it with the tag for the test suite. For example, for my tests in **features/getSaucey** the tag is `saucey`.

1. From the root of the project, run:

		curl -sS https://getcomposer.org/installer | php

2. Then run:

		php composer.phar install
		
3. From here, robo takes control, run:

		bin/robo init

4. For testing with Selenium `locally`, given selenium is running:

		bin/robo saucey:tipsy '<tag> <browser>'
	
	or, if you want to test with PhantomJS (Headless/Lightweight)
	
		bin/robo saucey:tipsy '<tag>'
		
	***Note: Not all tests will work with PhantomJS, i.e. @alert*

5. For testing against the `cloud`, you have to do three things (see [drunk](https://github.com/withpulp/saucey#cloud-w-saucelabs---drunk)). Set up SauceLabs to use your account:

		vendor/sauce/connect/bin/sauce_connect user_name access_key
		
	and:
		
		vendor/sauce_config user_name access_key
	
	then, run:

		bin/robo saucey:drunk '<tag> <environment> <browser>'

##Winery

1. Run the `Winery Test Suite` with:

		bin/robo winery:test

	Notice this opens `report/saucey_report_winery_test.html`

2. Additionally, you can just open the `winery` via:

		bin/robo winery
		
	Then, go to [http://127.0.0.1:7890](http://127.0.0.1:7890) 
	
	Be sure to checkout the `Browser-Based Inspector` @ [http://127.0.0.1:7890/client/#anonymous](http://127.0.0.1:7890/client/#anonymous)

##Shots! (examples)
###Local w/ [Selenium](http://docs.seleniumhq.org/) - Tipsy

1. Given you've installed via `init`, `install` & `bin/robo init` from above...
2. Run local examples via:

		bin/robo saucey:tipsy 'form firefox'

	or 
	
		bin/robo saucey:tipsy 'web chrome'
		
	or 

		bin/robo saucey:tipsy 'api'
		
	or 
		
		bin/robo saucey:tipsy 'shell'
		
3. Robo should be running the test suite, upon completion it should open a newly generated report.

4. `reports/saucey_report.html` should be opened, you should see a bunch of tests that look like:

```gherkin
Feature: SOAP & REST API Functionality

  As a tester
  I want to make sure api features are up and running
  So that I can automate continuous integration and regression tests using it

    @api @get
    Scenario: Make and validate a GET request
      Given send a GET request to "/comments?postId=1&id=1"
      Then  the response code should be 200
      And the response should contain json:
      """
        [
          {
            "postId": 1,
            "id": 1,
            "name": "id labore ex et quam laborum",
            "email": "Eliseo@gardner.biz",
            "body": "laudantium enim quasi est quidem magnam voluptate ipsam eos\ntempora quo necessitatibus\ndolor quam autem quasi\nreiciendis et nam sapiente accusantium"
          }
        ]
```

###Cloud w/ [SauceLabs](saucelabs.com) - Drunk
1. Given you've installed via `init`, `install` & `bin/robo init` from above...
2. To point **saucey** to SauceLabs, you'd need your `user_name` and `access_key`. Sign up and register for a **free** [SauceLabs](https://saucelabs.com/) account.
3. Get your username and api-key. *Should be available via /account.* Copy the info into your clipboard.
4. Open the `behat.yml` file with your favorite IDE and replace all instances of `username:api-key` with your username (used to log in) and api-key. Save.
5. Run a sanity suite via:  

		bin/robo saucey:drunk 'web mac chrome'

6. Then, go to [https://saucelabs.com/account](https://saucelabs.com/) and view your running/completed tests. Navigate through and download meta-data, screenshots and video recordings of the entire suite.
		
####localhost testing on the cloud
To test something on a localhost in the cloud, you can open a tunnel with sauce connect. With your username and api-key/access_key from the steps above, run:

	vendor/bin/sauce_config user_name access_key

To start the connect tunnel:

	vendor/sauce/connect/bin/sauce_connect 


###Mobile & Tablet
####For iOS:

	bin/robo saucey:drunk '<tag> ios_phone'

	bin/robo saucey:drunk '<tag> ios_tablet'

	bin/robo saucey:drunk '<tag> ios_tablet_landscape'

####For Android:

	bin/robo saucey:drunk '<tag> android_phone'

	bin/robo saucey:drunk '<tag> android_tablet'

	bin/robo saucey:drunk '<tag> android_tablet_landscape'



## Dependancies
On Mac OS X, (with the exception of LAMP for Windows) saucey requires the below dependancies. For now, the [Pour a glass](https://github.com/withpulp/saucey#pour-a-glass) section above should cover all dependancies. However, if there are errors thrown upon running `php composer.phar install` or `php composer.phar update` in terminal you can reference the sources below. They should also be maintained. 


1. [XCode](https://developer.apple.com/xcode/downloads/) & [Developer Tools](http://stackoverflow.com/questions/9329243/xcode-4-4-and-later-install-command-line-tools)
2. [Java JDK](http://www.oracle.com/technetwork/java/javase/downloads/jdk7-downloads-1880260.html), see [documentation](http://docs.oracle.com/javase/7/docs/webnotes/install/mac/mac-jdk.html)
3. [cURL](http://curl.haxx.se/download.html)
4. [WAMP](http://www.wampserver.com/en/) `Windows Only`
5. [PHP](http://php-osx.liip.ch/) *just incase, should be covered by composer.*
