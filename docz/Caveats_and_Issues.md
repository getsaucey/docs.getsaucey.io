#Caveats
1. To use the `local_safari` profile, in other words to test against a local version of Safari, go to:

	vendor/saucey/framework/drivers
	
2. And install the `safari_extension.cer`
3. Go `Safari`>`Preferences` and make sure it is enabled.

##Selenium Issues
The issues listed below are some known issues with the Selenium WebDriver.

1. Firefox ≤36.0.3 does not render ANY web driver functions from selenium, fixed in v36.0.4 with selenium 
2. Most of the major web driver functionality, i.e. pressing buttons, following links are completely non-functional for the Safari Web Driver.
3. Locally, some step definitions are non-functional: `iMoveBackwardOnePage`, `iMoveForwardOnePage`,`iRefreshThePage`

##Saucey Issues
See [https://github.com/withpulp/saucey/issues](https://github.com/withpulp/saucey/issues)

##TODO
See [https://github.com/withpulp/saucey/issues](https://github.com/withpulp/saucey/issues)
