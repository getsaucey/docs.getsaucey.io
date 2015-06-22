#docs.saucey.io
READ THE DOCS

##Clone
Open Terminal, and run:

	cd ~/Desktop && git clone git@github.com:sajjadhossain/AdcadeQADox.git

## `AUTHOR` get Mou 
1. Download [Mou](http://25.io/mou/). 
2. Navigate to `AdcadeQADox` folder in your Desktop. 
3. Then, open the `docs` folder. 
4. Right click on any .md file, i.e. `Click_Through_Verification.md` from `testing` folder & open with Mou.
5. Additionally, you can open Terminal and set Mou as an alias:

		alias mou="open /Applications/Mou.app"

	Please see: [Mou syntax](http://25.io/mou/), it comes with the install as well `COMMAND + R` when your in the app.

## `ADMINISTRATOR` get MkDocs 
Admins can also author via below.


## Commands

* `mkdocs new [dir-name]` - Create a new project.
* `mkdocs serve` - Start the live-reloading docs server.
* `mkdocs build` - Build the documentation site.
* `mkdocs build --clean` - Rebuilds the documentation site, cleans dependancies
* `mkdocs help` - Print this help message.

## Project layout

    mkdocs.yml    # The configuration file.
    docs/
        index.md  # The documentation homepage.
        ...       # Other markdown pages, images and other files.

---

#sauc·ey[*](http://www.urbandictionary.com/define.php?term=saucey)
[ /ˈsɑː-/ ] *intoxicated, drunk, or under the influence*
>Last night we went out to celebrate and got saucey at the bar off henessy.

##What this is?
Saucey is an Automation framework written in mainly PHP, using Behat and Mink. Designed to kick-ass and take names. 

##What it do?
This framework allows testers to:

* Control most aspects of the PC, i.e open a native iOS app with Xcode's iOS Simulator, etc.
* `Click`, `right-click`, `double-click`, `triple-click` & `drag` via X/Y coordinates.
* `Press any keyboard key(s)` either in conjunction or individually.
* `iOS/Android gestures`, i.e. 4-finger swipe left/right.
* Create & maintain tests for `Selenium` & headless drivers with [Gherkin](https://github.com/cucumber/cucumber/wiki/Gherkin).
* Evaluate `REST/SOAP API` endpoints with business-logic driven code.
* Run `load & performance` tests.
* Hook a Browser-Based Web Inspector to your app
* Assert against `Network/XHR` & `console logs`, DOM`, etc.
* Test UI elements with user-driven logic.
* Verify arrangement of files and directories; availability of assets.
* Set server-side, front-end and functional assertions.
* A reporting engine, with pass-fail statuses of all test cases, scenarios, and features
* Design `End-To-End`, `User Acceptance`, `Regression` & `Functional` test suites & cases
* Connect test suite(s) to a `continuous integration` system of choice.
* It's a Docker & Vagrant Image. Yes. The whole damn thing.



##What's inside

* [Selenium](http://docs.seleniumhq.org/)
* [PhantomJS](http://phantomjs.org/)
* [Behat](http://docs.behat.org/en/v3.0/)  
* [Pear](http://pear.php.net/)
* [Mink](http://mink.behat.org/en/latest/)  
* [JMeter](http://jmeter.apache.org/)
* [CLIClick](https://github.com/cucumber/cucumber/wiki/Gherkin)
* [Composer](https://getcomposer.org/)
* [Robo](https://github.com/Codegyre/Robo)
* [Weinre](http://people.apache.org/~pmuellr/weinre-docs/latest/Home.html)

##MOAR
* Find out more @ [http://saucey.io](http://saucey.io)  
* Fork the repo @ [https://github.com/withpulp/saucey.git](https://github.com/withpulp/saucey.git) 
* See [wiki](https://github.com/withpulp/saucey/wiki/)
	* See [The Winery](https://github.com/withpulp/saucey/wiki/The-Winery) for more on how this framework was set up.  
	* See [The Cellar](https://github.com/withpulp/saucey/wiki/The-Cellar) for available functionality.  