# Thunder Client
Thunder Client is a lightweight Rest API Client Extension for Visual Studio Code, hand-crafted by [Ranga Vadhineni](https://twitter.com/ranga_vadhineni) with simple and clean design. The source code is not open source. You can report any Bugs Or Feature requests here.

* Voted as **#10 Product of the day** on [Product Hunt](https://www.producthunt.com/posts/thunder-client)
* Website - [www.thunderclient.io](https://www.thunderclient.io)
* Follow Us for updates - [Twitter](https://twitter.com/thunder_client), [LinkedIn](https://www.linkedin.com/company/thunderclient/)

#### Story behind Thunder Client
* Read Launch Blog Post on [Medium](https://rangav.medium.com/thunder-client-alternative-to-postman-68ee0c9486d6)

## Review
* If you like this extension, please leave a review or rating on [VS Code Marketplace](https://marketplace.visualstudio.com/items?itemName=rangav.vscode-thunder-client), will be useful for new users.

## Menu
* [How to Use](#usage)
* [Tech](#tech)
* [Features](#features)
* [Team Features](#team)
* [Proxy](#proxy)
* [Import/Export](#import)
* [Run Collection](#runcol)
* [Scriptless Testing](#testing)
* [Keyboard Shortcuts](#keyboard)
* [Contribution](#contribution)
* [Privacy](#privacy)


<a name="usage"></a>
## How to Use
* Install the Extension, Click Thunder Client icon on the Action Bar.
* From Command Palette (Cm+Sh+P) type ``thunder`` and select ``Thunder Client: New Request``
* Video: [youtube.com/watch?v=NKZ0ahNbmak](https://www.youtube.com/watch?v=NKZ0ahNbmak)

![](images/thunder-client.gif)

<a name="tech"></a>
## Tech
* Thunder Client is built with **Javascript, Flexbox, Typescript, Ace Editor, Got, Nedb**. No javascript or bootstrap frameworks used.

<a name="features"></a>
## Features
* Send http/https API request using any of the methods GET, POST, PUT, DELETE, PATCH, HEAD and OPTIONS.
* The Response data supports **syntax hightlighting using ACE Editor** which can handle large responses easily, you can also view response in **Full Screen**
* **History, Collections and Environment** Tabs in the Action Bar View for quick access.
* **Authentication:** Basic Auth, Bearer Token and OAuth 2.0 are supported.
* **Headers:** You can send http headers to test api, with **auto-complete** support.
* **Post Body:** Send post body as Text, Json, Xml, Form Data, Files and Form-Url-Encoded. Content-Type header will be automatically set.
* **Graphql:** Send Graphql Query & Variables has syntax highlighting support.
* **Environment Variables:** Syntax highlighting support for environment variables just use `{{variable}}` syntax in most fields
* **Scriptless Testing:** Test APIs with GUI based functionality, no scripting knowledge needed.
* **Themes:** The extension also supports VS Code themes.

<a name="team"></a>
## Team Features
The team features are still in **Beta**, based on feedback I will improve it.

**WARNING**: There might be breaking changes for these Team features in next updates, so its not production ready.

* Integrate with the Git source control is now supported, 2 settings provided
* **Load From Project**: select this option when you like to spilt data per project, it will create `thunder-tests` folder in workspace. This loads the data when you open the project in vscode.
* **Custom Location**: select this option when you like save all the data in one location, enter the full folder path to save the data.
* Note 1: **Environment file**: if you dont want to save environment file to git server, use **gitignore** to ingore file thunderEnvironment.db
* Note 2: **Files changes** are not detected by the extension yet, if you pulled changes from git, click **Reload** option from collection Tab to update data.
* Note 3: Please **restart vscode** after updating settings.

<a name="proxy"></a>
## Proxy
Proxy is supported using vscode proxy setting. format `http://username:password@host:port`, please restart vscode after setting proxy.

<a name="import"></a>
## Import/Export
* You can import or export Thunder Client collections data, useful to share with team mates.
* Currently you can import collection or Environment file from **Postman** 2.1.0 format. ( other file formats support soon.. ).
* Submit PR for other file formats on https://github.com/rangav/thunder-imports

<a name="runcol"></a>
## Run Collection
* You can test multiple requests using Collection, select `Run All` option from the collection menu.
* The collection runner will execute all requests and test cases and display the result.

<a name="testing"></a>
## Scriptless Testing
![](https://github.com/rangav/thunder-client-support/blob/master/images/thunder-client-tests.png?raw=true)

* I noticed we need to write lot of boilerplate code in Postman and other clients to do basic testing using scripting like status code equal 200. So I implemented GUI based tests, where you select couple of dropdowns to do most standard tests very easily without any scripting knowledge.
* **Set Environment Variable** from tests tab is now supported, follow below steps
  * From the tests tab select `Set Env Variable` option and enter the json property
  * In value input enter the variable name when its matches name in Env, it will turn **green**, if variable not exists, it will create new.
  * Now execute the request you will see the variable value set in the Env.
  * **Set Variable from Text Response**: Enter `text` keyword in the left input
  * **Set Variable from Header**: Enter `header.headerName` in the left input, the prefix is `header.`
  * **Set Variable from Cookie**: Enter `cookie.cookieName` in the left input, the prefix is `cookie.`


<a name="keyboard"></a>
## Keyboard Shortcuts
* `Ctl+Shift+P`: From Command Palette
  * Thunder Client - New Request 
  * Thunder Client - Run Last Request
* `Cmd/Ctrl + Enter`: To execute the request
* `Cmd/Ctrl+s` Environment variable window save data.
* `Alt+Shft+f` Format Post Body data.

<a name="contribution"></a>
## Contribution Guidelines
* As the project is not open source, when you submit feature request or bug, if you know the solution, please submit code sample or a sample project in **node or .Net**, so it will be faster for me to integrate into main project. 

<a name="privacy"></a>
## Privacy
* Basic anonymised telemetry data of extension usage is collected using [vscode-extension-telemetry](https://github.com/Microsoft/vscode-extension-telemetry), No Personal or request data is collected. You can opt out using VS Code Settings [details here](https://code.visualstudio.com/docs/getstarted/telemetry)
* There is no backend or cloud sync currently, all the data is stored locally on your computer.


