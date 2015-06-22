The following information & step definitions are available by running: `vendor/bin/behat -di` or `vendor/bin/behat -dl` from the root of the repository.

**Words `highlighted` are variables**

##Available step definitions
A step definition is a single function that can be used in other functions, but truly shine when used in a scenario. A typical Behat scenario uses step definitions to execute tests. See [more](./link).

###Given I set my browser window size to `<width>` x `<height>`
Sets browser window to custom size  
**Examples:**
		
	Given I set browser window size to "1900" x "1200"
	When I set browser window size to "800" x "400"
	And I set browser window size to "2880" x "1800"

###Given I set my browser window size to MacBook Air
Sets browser window to 1440 by 900  
**Examples:**
		 
	Given I set my browser window size to MacBook Standard
	When I set my browser window size to MacBook Standard
	And I set my browser window size to MacBook Standard
   
###Given I set my browser window size to 15 inch MacBook Retina
Sets browser window to 2880 by 1800  
**Examples:**
		 
	Given I set my browser window size to 15 inch MacBook Retina
	When I set my browser window size to 15 inch MacBook Retina
	And I set my browser window size to 15 inch MacBook Retina

###Given I set my browser window size to 13 inch MacBook Retina
Sets browser window to 2560 by 1600  
**Examples:**
		 
    Given I set my browser window size to 13 inch MacBook Retina
    When I set my browser window size to 13 inch MacBook Retina
    And I set my browser window size to 13 inch MacBook Retina
    
###Given I set my browser window size to Windows Standard
Sets browser window to 1280 by 1280  
**Examples:**
		 
    Given I set my browser window size to Windows Standard
    When I set my browser window size to Windows Standard
	And I set my browser window size to Windows Standard
	
###When I set basic authentication with `<user>` and `<password>`
Set login / password for next HTTP authentication  
**Examples:**
		
	Given I set authentication with "bwayne" and "iLoveBats"
	When I set authentication with "bwayne" and "iLoveBats"
	And I set authentication with "bwayne" and "iLoveBats"

###Given I am on url composed by:
Open url with various parameters  
Change line:128 $url variable to url of choice    
**Examples:**
		
	Given I am on url composed by:
    | parameters |
    | /heroes    |
    | /batman    |
    
    When I am on url composed by:
    | parameters |
    | /heroes    |
    | /batman    |
    
    And I am on url composed by:
    | parameters |
    | /heroes    |
    | /batman    |

###When I click on the `<index>` `<element>` element
Clicks on the nth CSS element    
**Examples:**

	When I click on 1st "ul li a" element
	And I click on 6th "ul li a" element

###When I confirm the popup
Confirms the popup with "OK" press    
**Examples:**

	When I confirm the popup
	And I confirm the popup

###When I cancel the popup
Cancels the popup with "OK" press    
**Examples:**

	When I cancel the popup
	And I cancel the popup

###When I should see `<string>` in popup
Asserts string in popup    
**Examples:**

	And I should see "Bruce Wayne is not Batman" in popup
	Then I should see "Bruce Wayne is not Batman" in popup

###When I fill `<string>` in popup
Fills out popup field with text    
**Examples:**
	
	When I fill "Then why does he hang out with Dick Grayson?" in popup
	And I fill "Then why does he hang out with Dick Grayson?" in popup

###Given I scroll to the bottom
Scrolls to the bottom of the given page    
**Examples:**

	Given I scroll to the bottom
	When I scroll to the bottom
	And I scroll to the bottom

###Given I scroll to the top
Scrolls to the top of the given page    
**Examples:**

	Given I scroll to the top
	When I scroll to the top
	And I scroll to the top

###Given I scroll to the `<string>` field/link/button
Scroll to a certain element by label.   
Requires an "id" attribute to uniquely identify the element in the document.    
**Examples:**

	Given I scroll to the "Submit" button
	Given I scroll to the "My Date" field

###Given I am on a new session
Restarts Selenium session  
**Examples:**

	Given I am on a new session
	And I am on a new session

###When I click on the element with xpath `<XPath>`
Clicks on element via XPath  
**Examples:**

	When I click on the element with xpath '//*[@id="find-out-who-batman-is"]'
	And I click on the element with xpath '//*[@id="find-out-who-batman-is"]'

###Given I click on the element with xpath `<XPath>`
Clicks on element via XPath  
**Examples:**

	When I click on the element with xpath '//*[@id="find-out-who-batman-is"]'
	And I click on the element with xpath '//*[@id="find-out-who-batman-is"]'

###When I follow the `<index>` `<link>` link
**THIS FUNCTION IS CURRENTLY DEPRECATED AND NEEDS TLC**  
Click on the nth specified link  
**Examples:**

	When I click on 1st "ul li a" link
	And I click on 6th "ul li a" link

###When I fill in `<field>` with the current date
Fills in form field with current date  
**Examples:**

	When I fill in "unix-date" with the current date
	And I fill in "unix-date" with the current date

###When I fill in `<field>` with the current date and modifier :modifier
Fills in form field with current date and string to time (strtotime) modifier  
**Examples:**

	When I fill in "unix-date" with the current date and modifier "+1 day"
	And I fill in "unix-date" with the current date

###When I hover `<element>`
Mouse over a CSS element  
**Examples:**

	When I hover "large-button"
	And I hover "large-button"

###When I save the value of `<field>` in the `<parameter>` parameter
Save value of the field in parameters array  
**Examples:**

	When I save the value of "name" in the "name" parameter
	And I save the value of "name" in the "name" parameter

###Then I wait `<count>` second(s) until I see `<text>`
Checks, that the page should contains specified text after given timeout  
**Examples:**

	Given I wait 3 seconds until I see "Hello, Bruce Wayne"
	When I wait 3 seconds until I see "Hello, Bruce Wayne"
	And I wait 3 seconds until I see "Hello, Bruce Wayne"

###Then I wait until I see `<text>`
Checks, that the page should contains specified text after timeout  
**Examples:**

	Given I wait until I see "Hello, Bruce Wayne"	When I wait until I see "Hello, Bruce Wayne"
	And I wait until I see "Hello, Bruce Wayne"

###Then I wait `<count>` second(s) until I see `<text>` in the `<element>` element
Checks, that the element contains specified text after timeout  
**Examples:**

	Given I wait 3 seconds until I see "Hello, Bruce Wayne" in the "nav" element
	When I wait 3 seconds until I see "Hello, Bruce Wayne" in the "nav" element
	And I wait 3 seconds until I see "Hello, Bruce Wayne" in the "nav" element

###Then I wait until I see :text in the `<element>` element
Checks, that the element contains specified text after timeout  
**Examples:**

	Given I wait until I see "Hello, Bruce Wayne" in the "nav" element
	When I wait until I see "Hello, Bruce Wayne" in the "nav" element
	And I wait until I see "Hello, Bruce Wayne" in the "nav" element

###Then I wait `<count>` second(s) for `<element>` element
Wait for a element  
**Examples:**

	Given I wait 1 second for "sign-up" element
	When I wait 2 seconds for "sign-up" element
	And I wait 3 seconds for "sign-up" element

###Then I wait for `<element>` element
Checks, that the page should contains specified element after timeout  
**Examples:**

	Given I wait for "sign-up" element
	When I wait for "sign-up" element
	And I wait for "sign-up" element

###Then I wait `<count>` second(s)
Waits seconds  
**Examples:**

	Given I wait 1 second
	When I wait 2 second
	And I wait 3 seconds

###Given I wait for `<count>` seconds
Waits seconds  
**Examples:**

	Given I wait for 10 seconds
	When I wait for 9 seconds
	And I wait for 8 seconds

###Then I should see `<count>` `<element>` in the `<index>` `<parent>`
Asserts against number of elements in a response  
**Examples:**

	Then I should see 80 "div" in the 1st "body"
	And I should see 10 "li" in the 2nd "body"

###Then I should see less than `<count>` `<element>` in the `<index>` `<parent>`
Asserts against number of elements in a response  
**Examples:**

	Then I should see less than 199 "div" in the 1st "body"
	And I should see less than 200 "li" in the 1st "body"

###Then I should see more than `<count>` `<element>` in the `<index>` `<parent>`
Asserts against number of elements in a response  
**Examples:**

	Then I should see more than 10 "div" in the 1st "body"
	And I should see more than 1 "li" in the 1st "body"

###Then the element `<element>` should be enabled
Checks, that element with given CSS is enabled  
**Examples:**

	Then the element ".btn .btn-default" should be enabled
	And the element ".btn .btn-default" should be enabled

###Then the element `<element>` should be disabled
Checks, that element with given CSS is disabled  
**Examples:**

	Then the element ".btn .btn-default" should be disabled
	And the element ".btn .btn-default" should be disabled

###Then the `<select>` select box should contain :option
Checks, that given select box contains the specified option  
**Examples:**

	Then the "heroes" select box should contain "Batman"
	And the "heroes" select box should contain "Batman"

###Then the `<select>` select box should not contain :option
Checks, that given select box does not contain the specified option  
**Examples:**

	Then the "heroes" select box should not contain "Superman"
	And the "heroes" select box should not contain "Superman"

###Then the `<element>` element should be visible
Checks, that the specified CSS element is visible  
**Examples:**

	Then the ".btn" element should be visible
	And the ".btn" element should be visible

###Then the `<element>` element should not be visible
Checks, that the specified CSS element is not visible  
**Examples:**

	Then the ".btn" element should not be visible
	And the ".btn" element should not be visible

###When I switch to iframe `<name>`
Select a frame by its name or ID 
**Examples:**

	When I switch to iframe "justAnotherIframe"
	And I switch to frame "justAnotherIframe"

###When I switch to frame `<name>`
Select a frame by its name or ID  
**Examples:**

	When I switch to iframe "justAnotherIframe"
	And I switch to frame "justAnotherIframe"

###When I switch to main frame
Go back to main document frame  
**Examples:**

	When I switch to main frame
	And I switch to main frame

###Then I put a breakpoint
Pauses the scenario until the user presses a key. Useful when debugging a scenario.  
**Examples:**

	When I put a breakpoint
	Then I put a breakpoint
	And I put a breakpoint

###When I save a screenshot in `<filename>`
Saving a screenshot  
**Examples:**

	When I save a screenshot in "logInView"
	Then I save a screenshot in "logInView"
	And I save a screenshot in "logInView"

###Given I am in `<dir>` directory
Changes directory to :directory requested.  
**Examples:**

	Given I am in "/Users/bWayne/secretfiles/batman"
	And I am in "/Users/bWayne/secretfiles/batman"

###When I run `<command>`
Runs a command line argument  
**Examples:**

	When I run ".openCaveEntrance"
	And I run ".openCaveEntrance"

###When I put the file `<file>` into `<field>`
Uploads a file using the specified input field  
**Examples:**

	Given I put the file "batman_profile.jpg" into "heroImage"
	When I put the file "batman_profile.jpg" into "heroImage"
	And I put the file "batman_profile.jpg" into "heroImage"

###Given I execute `<command>`
Execute a command  
**Examples:**

	Given I execute "pwd"
	When I execute "pwd"
	And I execute "pwd"

###Given I execute `<command>` from project root
Execute a command from project root  
**Examples:**

	Given I execute "php ./openBatCave.php" from project root
	When I execute "php ./openBatCave.php" from project root
	And I execute "php ./openBatCave.php" from project root

###Given I create the file `<filename>` containing:
Creates a file via touch command  
**Examples:**

	Given I create the file "batmansPasswords.txt" containing"
    """
    Facebook: RIPMarthaThomas1927
    Twitter: RIPTimothyDrake1986
    Netflix: RIPDamianWayne2009
    Google: DamnIveSeenSomeStuff
    """
    
    When I create the file "batmansPasswords.txt" containing"
    """
    Facebook: RIPMarthaThomas1927
    Twitter: RIPTimothyDrake1986
    Netflix: RIPDamianWayne2009
    Google: DamnIveSeenSomeStuff
    """

	And I create the file "batmansPasswords.txt" containing"
    """
    Facebook: RIPMarthaThomas1927
    Twitter: RIPTimothyDrake1986
    Netflix: RIPDamianWayne2009
    Google: DamnIveSeenSomeStuff
    """

###Then print the content of `<filename>` file
Prints the content of passed file  
**Examples:**

	Given I print the content of "./batmansGreatestSecrets.txt" file
	When I print the content of "./batmansGreatestSecrets.txt" file
	Then I print the content of "./batmansGreatestSecrets.txt" file

###Then I should see:
Asserts against previously run command line argument.  
**Examples:**

	Then I should see:
	"""
	Opening cave, master Bruce.
	"""
	
	And I should see:
	"""
	Opening cave, master Bruce.
	"""

###Then the response should be in JSON
Checks, that the response is correct JSON  
**Examples:**

	Then the response should be in JSON
	And the response should be in JSON

###Then the response should not be in JSON
Checks, that the response is not correct JSON  
**Examples:**

	Then the response should not be in JSON
	And the response should not be in JSON

###Then the JSON node `<node>` should be equal to :text
Checks, that given JSON node is equal to given value  
**Examples:**

	Then the JSON node "isBatman"should be equal to "true"
	And the JSON node "isBatman" should be equal to "true"

###Then the JSON node `<node>` should have `<count>` element(s)
Checks, that given JSON node has N element(s)  
**Examples:**

	Then the JSON node "bio" should have 5 elements
	And the JSON node "bio" should have 5 elements

###Then the JSON node `<node>` should contain :text
Checks, that given JSON node contains given value  
**Examples:**

	Then the JSON node "trueIdentity" should contain "Bruce Wayne"
	And the JSON node "trueIdentity" should contain "Bruce Wayne"

###Then the JSON node `<node>` should not contain :text
Checks, that given JSON node does not contain given value  
**Examples:**

	Then the JSON node "isRobin" should not contain "true"
	And the JSON node "isRobin" should not contain "true"

###Given the JSON node `<name>` should exist
Checks, that given JSON node exist  
**Examples:**

	Given the JSON node "id" should exist
	Then the JSON node "id" should exist
	And the JSON node "id" should exist

###Given the JSON node `<name>` should not exist
Checks, that given JSON node does not exist  
**Examples:**

	Given the JSON node "Robin" should not exist
	Then the JSON node "Robin" should not exist
	And the JSON node "Robin" should not exist

###Then the JSON should be valid according to this schema:
Checks provided JSON against a JSON schema  
**Examples:**

	Then the JSON should be valid according to this schema:
	"""
	{
		"$schema": "http://json-schema.org/draft-04/schema#",
		"title": "Heroes",
		"description": "A list of heroes from the known universe",
		"type": "object",
			"properties": {
				"id": {
					"description": "The unique identifier for a hero",
					"type": "integer"
				},
				"name": {
					"description": "Name of the hero",
					"type": "string"
				},
				"alterEgo": {
					"description": "Alter ego for hero",
					"type": "string"
				}
			},
		"required": ["id", "name", "alterEgo"]
	}
	"""
	
	And the JSON should be valid according to this schema:
	"""
	{
		"$schema": "http://json-schema.org/draft-04/schema#",
		"title": "Heroes",
		"description": "A list of heroes from the known universe",
		"type": "object",
			"properties": {
				"id": {
					"description": "The unique identifier for a hero",
					"type": "integer"
				},
				"name": {
					"description": "Name of the hero",
					"type": "string"
				},
				"alterEgo": {
					"description": "Alter ego for hero",
					"type": "string"
				}
			},
		"required": ["id", "name", "alterEgo"]
	}
	"""

###Then the JSON should be valid according to the schema `<filename>`
Checks provided JSON against a provided JSON schema  
**Examples:**

	Then the JSON should be valid according to the schema "http://batman.com/secret-schema"
	And the JSON should be valid according to the schema "http://batman.com/secret-schema"

###Then the JSON should be equal to:
Checks that the JSON response is equal to value  
**Examples:**

	Then the JSON should be equal to:
	"""
	{
		"id": 1,
		"name": "Batman",
		"alterEgo": "Bruce Wayne"
	}
	"""
	
	And the JSON should be equal to:
	"""
	{
		"id": 1,
		"name": "Batman",
		"alterEgo": "Bruce Wayne"
	}
	"""

###Then print last JSON response
Prints last JSON response  
**Examples:**

	Then print last JSON response
	And print last JSON response

###Then the columns schema of the `<table>` table should match:
Checks that the specified table's columns match the given schema  
**Examples:**

	Then the columns schema of the "heroes" table should match:
	| hero_id | hero_name | alter_ego |
	
	And the columns schema of the "heroes" table should match:
	| hero_id | hero_name | alter_ego |

###Then I should see `<count>` column(s) in the `<table>` table
Checks that the specified table contains the given number of columns  
**Examples:**

	Then I should see 4 columns in the "heroes" table
	And I should see 4 columns in the "heroes" table

###Then I should see `<count>` rows in the `<index>` `<table>` table
Checks that the specified table contains the specified number of rows in its body  
**Examples:**

	Then I should see 4 rows in the "hero_body" "heroes" table
	And I should see 4 rows in the "hero_body" "heroes" table

###Then I should see `<count>` row(s) in the `<table>` table
Checks that the specified table contains the specified number of rows in its body  
**Examples:**

	Then I should see 500 rows in the "heroes" table
	And I should see 500 rows in the "heroes" table

###Then the data in the `<index>` row of the `<table>` table should match:
Checks that the data of the specified row matches the given schema  
**Examples:**

	Then the data in the 4th row of the "heroes" table should match:
	| 1 | Batman | Bruce Wayne |
	
	And the data in the 4th row of the "heroes" table should match:
	| 1 | Batman | Bruce Wayne |

###Then the `<colIndex>` column of the `<rowIndex>` row in the `<table>` table should contain `<text>`
Checks that the specified cell (column/row) of the table's body contains the specified text  
**Examples:**

	Then the 1st column of the 4th row in the "heroes" table should contain "Aquaman"
	Then the 1st column of the 5th row in the "heroes" table should contain "Wonder Woman"

###Given I send a `<method>` request to `<url>`
Sends a HTTP request  
**Examples:**

	Given I send a GET request to "/heroes/list"
	When I send a GET request to "/heroes/list"
	And I send a GET request to "/heroes/list"

###Given I send a `<method>` request to `<url>` with parameters:
Sends a HTTP request with a some parameters  
**Examples:**

	Given I send a GET request to "/heroes/list" with parameters:
	| userId | 27 |
	| username | bruceWayne |
	| password | iLoveBats123 |
	
	When I send a GET request to "/heroes/list" with parameters:
	| userId | 27 |
	| username | bruceWayne |
	| password | iLoveBats123 |
	
	And I send a GET request to "/heroes/list" with parameters:
	| userId | 27 |
	| username | bruceWayne |
	| password | iLoveBats123 |

###Given I send a `<method>` request to `<url>` with body:
Sends a HTTP request with a body  
**Examples:**

	Given I send a GET request to "/heroes/list" with body:
	"""
	{
		{
			"body": "I am not batman I take serious offense to any claims suggesting such outlandish remarks.",
			"id" : 1
		}
	}
	"""
	
	When I send a POST request to "/heroes/list" with form data:
	"""
	{
		{
			"body": "I am not batman I take serious offense to any claims suggesting such outlandish remarks.",
			"id" : 1
		}
	}
	"""
	
	And I send a GET request to "/heroes/list" with body:
	"""
	{
		{
			"body": "I am not batman I take serious offense to any claims suggesting such outlandish remarks.",
			"id" : 1
		}
	}
	"""

###Then the response should be equal to:
Checks, whether the response content is equal to given text  
**Examples:**

	Then the response should be equal to
	"""
	{
		{
			"body": "Bruce Wayne, billionaire playboy.",
			"id" : 1
		}
	}
	"""
	
	And the response should be equal to
	"""
	{
		{
			"body": "Bruce Wayne, billionaire playboy.",
			"id" : 1
		}
	}
	"""

###Then the response should be empty
Checks, whether the response content is null or empty string  
**Examples:**

	Then the response should be empty
	And the response should be empty

###Then the header `<name>` should be equal to `<value>`
Checks, whether the header name is equal to given text  
**Examples:**

	Then the header "User-Agent" should be equal to "Batbook, BatBrowser"
	And the header "User-Agent" should be equal to "Batbook, BatBrowser"

###Then the header `<name>` should contain `<value>`
Checks, whether the header name contains the given text  
**Examples:**

	Then the header "Authentication" should contain "1024 Bit Super-Authenticated"
	And the header "Authentication" should contain "1024 Bit Super-Authenticated"

###Then the header :name should not contain :value
Checks, whether the header name doesn't contain the given text  
**Examples:**

	Then the header "" should contain "1024 Bit Super-Authenticated"
	And the header "Authentication" should contain "1024 Bit Super-Authenticated"

###Then the header :name should not exist
        | Checks, whether the header not exist
        | Example: Then the header "Content-Type" should not exist
        | Example: And the header "Content-Type" should not exist
        | at `Sanpi\Behatch\Context\RestContext::theHeaderShouldNotExist()`

###Then the response should expire in the future
Checks, that the response header expire is in the future  
**Examples:**

	Then the response should expire in the future
	And the response should expire in the future

###Then I add `<name>` header equal to `<value>`
        | Add an header element in a request
        | Example: Then I add "Content-Type" header equal to "application/json"
        | Example: And I add "Content-Type" header equal to "application/json"
        | at `Sanpi\Behatch\Context\RestContext::iAddHeaderEqualTo()`

###Then the response should be encoded in `<encoding>`
Asserts against responses encoding type, see [http://www.iana.org/assignments/character-sets/character-sets.xhtml](http://www.iana.org/assignments/character-sets/character-sets.xhtml)  
**Examples:**

	Then the response should be encoded in "UTF-8"
	And the response should be encoded in "UTF-8"

###Then print last response headers
Prints last response  
**Examples:**

	Then print last response headers

###Then print the corresponding curl command
Prints the curl equivalent to the request  
**Examples:**

	Then print the corresponding curl command

###Then the response should be in XML
Checks that the response is correct XML  
**Examples:**

	Then the response should be in XML
	And the response should be in XML

###Then the response should not be in XML
Checks that the response is not correct XML  
**Examples:**

	Then the response should not be in XML
	And the response should not be in XML

###Then the XML element `<element>` should exist(s)
Checks that the specified XML element exists  
**Examples:**

	Then the XML element "Vehicles" should exist
	And the XML element "Vehicles" should exist

###Then the XML element `<element>` should not exist(s)
Checks that the specified XML element does not exist  
**Examples:**

	Then the XML element "Suits" should not exist
	And the XML element "Suits" should exist

###Then the XML element `<element>` should be equal to `<text>`
Checks that the specified XML element is equal to the given value  
**Examples:**

	Then the XML element "Vehicles" should be equal to "Batmobile, Batwing, Batboat, Battank"
	And the XML element "Vehicles" should be equal to "Batmobile, Batwing, Batboat, Battank"

###Then the XML element `<element>` should not be equal to `<text>`
Checks that the specified XML element is not equal to the given value  
**Examples:**

	Then the XML element "Suits" should not be equal to "Santiago's BatSuit"
	And the XML element "Suits" should not be equal to "Santiago's BatSuit"

###Then the XML attribute `<attribute>` on element `<element>` should exist(s)
Checks that the XML attribute on the specified element exists  
**Examples:**

	Then the XML attribute "VehicleID" on element "Vehicles" should exist
	And the XML attribute "VehicleID" on element "Vehicles" should exist

###Then the XML attribute `<attribute>` on element `<element>` should not exist(s)
Checks that the XML attribute on the specified element does not exist  
**Examples:**

	Then the XML attribute "VehicleID" on element "Vehicles" should not exist
	And the XML attribute "VehicleID" on element "Vehicles" should not exist

###Then the XML attribute `<attribute>` on element `<element>` should be equal to `<text>`
Checks that the XML attribute on the specified element is equal to the given value  
**Examples:**

	Then the XML attribute "VehicleName" on element "Vehicles" should be equal to "Batmobile"
	And the XML attribute "VehicleName" on element "Vehicles" should be equal to "Batmobile"

###Then the XML attribute `<attribute>` on element `<element>` should not be equal to `<text>`
Checks that the XML attribute on the specified element is not equal to the given value  
**Examples:**

	Then the XML attribute "SuitOwner" on element "Suits" should not be equal to "David Zavimbe"
	And the XML attribute "SuitOwner" on element "Suits" should not be equal to "David Zavimbe"

###Then the XML element `<element>` should have `<count>` element(s)
Checks that the given XML element has N child element(s)  
**Examples:**

	Then the XML element "Vehicles" should have "6" elements
	And the XML element "Vehicles" should have "6" elements

###Then the XML element `<element>` should contain `<text>`
Checks that the given XML element contains the given value  
**Examples:**

	Then the XML element "VehicleName" should contain "Batmobile"
	And the XML element "VehicleName" should contain "Batmobile"

###Then the XML element 	`<element>` should not contain `<text>`
Checks that the given XML element does not contain the given value  
**Examples:**

	Then the XML element "VehicleName" should not contain "Batsub"
	And the XML element "VehicleName" should not contain "Batsub"

###Then the XML should use the namespace `<namespace>`
Checks that the XML uses the specified namespace  
**Examples:**

	Then the XML should use the namespace "Batman"
	And the XML should use the namespace "Batman"

###Then the XML should not use the namespace `<namespace>`
Checks that the XML does not use the specified namespace  
**Examples:**

	Then the XML should not use the namespace "Robin"
	And the XML should not use the namespace "Robin"

###Then print last XML response
Optimistically (ignoring errors) attempt to pretty-print the last XML response  
**Examples:**

	Then print last XML response

###Then the XML feed should be valid according to its DTD
Checks validity of XML against a DTD  
**Examples:**

	Then the XML feed should be valid according to its DTD
	And the XML feed should be valid according to its DTD

###Then the XML feed should be valid according to the XSD `<filename>`
Checks validity of XML against a provided XSD  
**Examples:**

	Then the XML feed should be valid according to the XSD "batman.xsd"
	And the XML feed should be valid according to the XSD "batman.xsd"

###Then the XML feed should be valid according to this XSD:
Checks validity of XML against a provided XSD  
**Examples:**

	Then the XML feed should be valid according to this XSD:
    """
    <?xml version="1.0"?>
    <xs:schema xmlns:xs="http://www.w3.org/2001/XMLSchema">
    <xs:element name="note">
    <xs:complexType>
    <xs:sequence>
    <xs:element name="to" type="xs:string"/>
    <xs:element name="from" type="xs:string"/>
    <xs:element name="heading" type="xs:string"/>
    <xs:element name="body" type="xs:string"/>
    </xs:sequence>
    </xs:complexType>
    </xs:element>
    </xs:schema>
    """
	
	And the XML feed should be valid according to this XSD:
	"""
    <?xml version="1.0"?>
    <xs:schema xmlns:xs="http://www.w3.org/2001/XMLSchema">
    <xs:element name="note">
    <xs:complexType>
    <xs:sequence>
    <xs:element name="to" type="xs:string"/>
    <xs:element name="from" type="xs:string"/>
    <xs:element name="heading" type="xs:string"/>
    <xs:element name="body" type="xs:string"/>
    </xs:sequence>
    </xs:complexType>
    </xs:element>
    </xs:schema>
    """

###Then the XML feed should be valid according to the relax NG schema `<filename>`
Checks validity of XML against a provided RELAX NG Schema  
**Examples:**

	Then the XML feed should be valid according to the relax NG schema "batman.xsd"
	And the XML feed should be valid according to the relax NG schema "batman.xsd"

###Then the XML feed should be valid according to this relax NG schema:
Checks validity of XML against a provided RELAX NG Schema  
**Examples:**

	Then the XML feed should be valid according to this relax NG schema:
    """
    <element name="book" xmlns="http://relaxng.org/ns/structure/1.0">
    <oneOrMore>
    <element name="page">
    <text/>
    </element>
    </oneOrMore>
    </element>
    """
	
	And the XML feed should be valid according to this relax NG schema:
    """
    <element name="book" xmlns="http://relaxng.org/ns/structure/1.0">
    <oneOrMore>
    <element name="page">
    <text/>
    </element>
    </oneOrMore>
    </element>
    """

###Then the atom feed should be valid
Checks the validity of the atom XML feed  
**Examples:**

	Then the atom feed should be valid

###Then the RSS2 feed should be valid
Checks the validity of the RSS2 feed  
**Examples:**

	Then the RSS2 feed should be valid

###Then I go to network tab
Wienre: Shifts focus to Network tab  
**Examples:**

	When I go to network tab
	Then I go to network tab
	And I go to network tab

###Then I go to elements tab
Wienre: Shifts focus to Elements tab  
**Examples:**

	When I go to elements tab
	Then I go to elements tab
	And I go to elements tab

###Then I go to console tab
Wienre: Shifts focus to console tab  
**Examples:**

	When I go to console tab
	Then I go to console tab
	And I go to console tab

###Then I select request `<number>`
Wienre: Shifts focus to Network tab for a given request  
**Examples:**

	When I select request 1
	Then I select request 1
	And I select request 1

###Then I am on the network header tab
Wienre: Shifts focus to Network header tab  
**Examples:**

	When I go to network header tab
	Then I go to network header tab
	And I go to network header tab

###Given I am on (the) homepage
Opens homepage  
**Examples:**

	Given I am on "/"
	When I go to "/"
	And I go to "/"

###When I go to (the) homepage
Opens homepage  
**Examples:**

	Given I am on "/"
	When I go to "/"
	And I go to "/"

###Given I am on (the) `<page>`
Opens specified page  
**Examples:**

	Given I am on "http://batman.com"
	When I am on "http://batman.com"
	And I go to "http://batman.com"

###When I go to `<page>`
Opens specified page  
**Examples:**

	Given I am on "http://batman.com"
	When I am on "http://batman.com"
	And I go to "http://batman.com"

###When I reload the page
Reloads current page  	
**Examples:**

	Given I reload the page
	When I reload the page
	And I reload the page

###When I move backward one page
Moves backward one page in history  
**Examples:**

	Given I move backward one page
	When I move backward one page
	And I move backward one page

###When I move forward one page
Moves forward one page in history  
**Examples:**

	Given I move forward one page
	When I move forward one page
	And I move forward one page

###When I press `<button>`
Presses button with specified id|name|title|alt|value  
**Examples:**

	Given I press "Log In"
	When I press "Log In"
	And I press "Log In"

###When I follow `<link>`
Clicks link with specified id|title|alt|text  
**Examples:**

	Given I follow "Log In"
	When I follow "Log In"
	And I follow "Log In"

###When I fill in `<field>` with `<value>`
Fills in form field with specified id|name|label|value  
**Examples:**

	Given I fill in "username" with "bwayne"
	When I fill in "username" with: "bwayne"
	And I fill in "bwayne" for "username"

###When I fill in `<field>` with:
Fills in form field with specified id|name|label|value  
**Examples:**

	Given I fill in "username" with "bwayne"
	When I fill in "username" with: "bwayne"
	And I fill in "bwayne" for "username"

###When I fill in `<value>` for `<field>`
Fills in form field with specified id|name|label|value  
**Examples:**

	Given I fill in "username" with "bwayne"
	When I fill in "username" with: "bwayne"
	And I fill in "bwayne" for "username"

###When I fill in the following:
Fills in form fields with provided table  
**Examples:**

	Given I fill in the following"
	| username | bruceWayne |
	| password | iLoveBats123 |
	
	When I fill in the following"
	| username | bruceWayne |
	| password | iLoveBats123 |
	
	And I fill in the following"
	| username | bruceWayne |
	| password | iLoveBats123 |

###When I select `<option>` from `<select>`
Selects option in select field with specified id|name|label|value  
**Examples:**

	Given I select "Bats" from "user_fears"
	When I select "Bats" from "user_fears"
	And I select "Bats" from "user_fears"

###When I additionally select `<option>` from `<select>`
Selects additional option in select field with specified id|name|label|value  
**Examples:**

	Given I additionally select "Deceased" from "parents_alive_status"
	When I additionally select "Deceased" from "parents_alive_status"
	And I additionally select "Deceased" from "parents_alive_status"

###When I check `<option>` from `<name>`
Checks checkbox with specified id|name|label|value  
**Examples:**

	Given I check "Pearl Necklace" from "itemsClaimed"
	When I check "Pearl Necklace" from "itemsClaimed"
	And I check "Pearl Necklace" from "itemsClaimed"

###When I uncheck `<option>` from `<name>`
Unchecks checkbox with specified id|name|label|value  
**Examples:**

	Given I uncheck "Broadway Plays" from "hobbies"
	When I uncheck "Broadway Plays" from "hobbies"
	And I uncheck "Broadway Plays" from "hobbies"

###When I attach the file `<path>` to `<field>`
Attaches file to field with specified id|name|label|value  
**Examples:**

	Given I attach "bwayne_profile.png" to "profileImageUpload"
	When I attach "bwayne_profile.png" to "profileImageUpload"
	And I attach "bwayne_profile.png" to "profileImageUpload"

###Then I should be on `<page>`
Checks, that current page PATH is equal to specified  
**Examples:**

	Then I should be on "/"
	And I should be on "/bats"
	And I should be on "http://google.com"

###Then I should be on (the) homepage
        | Checks, that current page is the homepage.
        | Example: Then I should be on the homepage
        | Example: And I should be on the homepage
        | at `FeatureContext::assertHomepage()`

###Then the url should match `<pattern>`
Checks, that current page PATH matches regular expression  
**Examples:**

	Then the url should match "superman is dead"
	Then the uri should match "log in"
	And the url should match "log in"

###Then the response status code should be `<code>`
Checks, that current page response status is equal to specified  
**Examples:**

	Then the response status code should be 200
	And the response status code should be 400

###Then the response status code should not be `<code>`
Checks, that current page response status is not equal to specified  
**Examples:**

	Then the response status code should not be 501
	And the response status code should not be 404

###Then I should see `<text>`
Checks, that page contains specified text  
**Examples:**

	Then I should see "Who is the Batman?"
	And I should see "Who is the Batman?"

###Then I should not see `<text>`
Checks, that page doesn't contain specified text  
**Examples:**

	Then I should not see "Batman is Bruce Wayne"
	And I should not see "Batman is Bruce Wayne"

###Then I should see text matching `<pattern>`
Checks, that page contains text matching specified pattern  
**Examples:**

	Then I should see text matching "Batman, the vigilante"
	And I should not see "Batman, the vigilante"

###Then I should not see text matching `<pattern>`
Checks, that page doesn't contain text matching specified pattern  
**Examples:**

	Then I should see text matching "Bruce Wayne, the vigilante"
	And I should not see "Bruce Wayne, the vigilante"

###Then the response should contain `<text>`
Checks, that HTML response contains specified string  
**Examples:**

	Then the response should contain "Batman is the hero Gotham deserves."
	And the response should contain "Batman is the hero Gotham deserves."

###Then the response should not contain `<text>`
Checks, that HTML response doesn't contain specified string  
**Examples:**

	Then the response should not contain "Bruce Wayne is a billionaire, play-boy, vigilante."
	And the response should not contain "Bruce Wayne is a billionaire, play-boy, vigilante."

###Then I should see `<text>` in the `<element>` element
        | Checks, that element with specified CSS contains specified text.
        | Example: Then I should see "Batman" in the "heroes_list" element
        | Example: And I should see "Batman" in the "heroes_list" element
        | at `FeatureContext::assertElementContainsText()`

###Then I should not see `<text>` in the `<element>` element$/
Checks, that element with specified CSS doesn't contain specified text  
**Examples:**

	Then I should not see "Bruce Wayne" in the "heroes_alter_egos" element
	And I should not see "Bruce Wayne" in the "heroes_alter_egos" element

###Then the `<element>` element should contain `<value>`
Checks, that element with specified CSS contains specified HTML  
**Examples:**

	Then the "body" element should contain "style=\"color:black;\""
	And the "body" element should contain "style=\"color:black;\""

###Then the `<element>` element should not contain `<value>`
Checks, that element with specified CSS doesn't contain specified HTML  
**Examples:**

	Then the "body" element should not contain "style=\"color:black;\""
	And the "body" element should not contain "style=\"color:black;\""

###Then I should see a(n) `<element>` element
        | Checks, that element with specified CSS exists on page.
        | Example: Then I should see a "body" element
        | Example: And I should see a "body" element
        | at `FeatureContext::assertElementOnPage()`

###Then I should not see a(n) `<element>` element
Checks, that element with specified CSS doesn't exist on page  
**Examples:**

	Then I should not see a "canvas" element
	And I should not see a "canvas" element

###Then the `<field>` field should contain `<value>`
Checks, that form field with specified id|name|label|value has specified value  
**Examples:**

	Then the "username" field should contain "bwayne"
	And the "username" field should contain "bwayne"

###Then the `<field>` field should not contain `<value>`
Checks, that form field with specified id|name|label|value doesn't have specified value  
**Examples:**

	Then the "username" field should not contain "batman"
	And the "username" field should not contain "batman"

###Then the `<checkbox>` checkbox should be checked
Checks, that checkbox with specified in|name|label|value is checked  
**Examples:**

	Then the "remember_me" checkbox should be checked
	And the "remember_me" checkbox is checked

###Then the checkbox `<checkbox>` (is|should be) checked
Checks, that checkbox with specified in|name|label|value is checked  
**Examples:**

	Then the "remember_me" checkbox should be checked
	And the "remember_me" checkbox is checked

###Then the `<checkbox>` checkbox should not be checked
Checks, that checkbox with specified in|name|label|value is unchecked  
**Examples:**

	Then the "newsletter" checkbox should be unchecked
	Then the "newsletter" checkbox should not be checked
	And the "newsletter" checkbox is unchecked

###Then the checkbox `<checkbox>` should (be unchecked|not be checked)
Checks, that checkbox with specified in|name|label|value is unchecked  
**Examples:**

	Then the "newsletter" checkbox should be unchecked
	Then the "newsletter" checkbox should not be checked
	And the "newsletter" checkbox is unchecked
	
###Then the checkbox `<checkbox>` is (unchecked|not checked)
Checks, that checkbox with specified in|name|label|value is unchecked  
**Examples:**

	Then the "newsletter" checkbox should be unchecked
	Then the "newsletter" checkbox should not be checked
	And the "newsletter" checkbox is unchecked

###Then I should see `<int>` `<element>` elements
Checks, that count CSS elements exist on the page  
**Examples:**

	Then I should see 5 "div" elements
	And I should see 5 "div" elements

###Then print current URL
Prints current URL to console  
**Examples:**

	Then print current URL
	And print current URL

###Then print last response
Prints last response to console  
**Examples:**

	Then print current response
	And print current response

###Then show last response
Opens last response content in browser.
        | Example: Then show last response
        | Example: And show last response
        | at `FeatureContext::showLastResponse()`

###Given I tap `<x>` x `<y>` coordinates
Clicks or taps based on x,y coordinates  
**Examples:**

	When I tap "10" x "10" coordinates
	And I tap "10" x "10" coordinates

###Given I initiate drag at `<x>` x `<y>` coordinates
Initiates drag based on x,y coordinates  
**Examples:**

	When I initiate drag at "10" x "10" coordinates
	And I initiate drag at "10" x "10" coordinates

###Given I release drag at `<x>` x `<y>` coordinates
Releases drag based on x,y coordinates  
**Examples:**

	When I release drag at "10" x "10" coordinates
	And I release drag at "10" x "10" coordinates

###When I move to `<x>` x `<y>` coordinates
Moves mouse based on x,y coordinates  
**Examples:**

	When I move to "10" x "10" coordinates
	And I move to "10" x "10" coordinates

###Given I move along x axis `<x>` from y `<y1>` to `<y2>`
Moves mouse along x axis based on x, y1 & y2 coordinates  
**Examples:**

	When I move along x axis "10" from y "10" to "20"
	And I move along x axis "10" from y "10" to "20"

###Given I move along y axis `<y>` from x `<x1>` to `<x2>`
Moves mouse along y axis based on y, x1 & x2 coordinates  
**Examples:**

	When I move along y axis "10" from x "10" to "20"
	And I move along y axis "10" from x "10" to "20"

###Given I drag from `<xy1>` to `<xy2>`
Initiates drag, then drags from x1,y1 to x2,y2, then releases  
**Examples:**

	When I drag from "100,100" to "200,200"
	And I drag from "100,100" to "200,200"

###Given I move from `<xy1>` to `<xy2>`
Moves from x1,y1 to x2,y2  
**Examples:**

	When I move from "100,100" to "200,200"
	And I move from "100,100" to "200,200"
