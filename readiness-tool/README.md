
# AMP Readiness Chrome Extension

## Introduction: 
The AMP Readiness Tool (ART) is designed to assist in determining whether AMP can be incorporated into a website's existing mobile page. The tool examines, via Chrome Extension, the different services, ads and analytics networks utilized on the page and specifies whether each service currently has AMP support. For the services that aren't supported, workarounds and substitutions will be given in order for the Sales team to better estimate the time and energy required for the website to become an AMP page.

## Using the tool: 
1. Direct your Chrome tab towards whose AMP-readiness you wish to inspect
2. Click the AMP Readiness Tool Chrome Extension in your toolbar
3. Wait for the data to load
4. Enjoy!

## Instructions to get ART in your Chrome browser:
1. Download the [zip file](https://github.com/ampproject/ampbench/archive/master.zip). 
2. Unzip the file.
3. While in the Chrome browser, type `chrome://extensions/` into the omnibox
4. Make sure that "Developer Mode" in the top right corner is checked
5. Click the "Load the unpacked extension..." button 
6. Direct the window to where your unzipped file and into the readiness-tool folder

## Updating the list of Third Party Vendors:

Here is a sample of how the third party vendor should be included in the apps.json file. This file contains the names of all applicable third party vendors on the page. Each vendor contains a "cats" value and a "script" value.

`Cats` - (abbreviation of categories) it's value has a numeric representation that coordinates to the key of the same name inside the "categories" object at the foot of the page. A value of "36" indicates that it is an analytics service and a value of "10" indicates an ads network.

`Script` - a regular expression that is unique to that vendor

Below is an example of the Google Analytics tag.
```
{
    "apps": {
        "Google Analytics": {
			      "cats": [
				      "36"
			      ],
			    "script": [
				      "googlesyndication\\.com/",
				      "ad\\.ca\\.doubleclick\\.net"
			      ]
         }
     }
}
```


                  
