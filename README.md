## Develop and Host Chrome Extension in 4 Steps.

## What are extensions?

Extensions are small software programs that customize the browsing experience. They enable users to tailor Chrome functionality and behavior to individual needs or preferences. They are built on web technologies such as HTML, JavaScript, and CSS.

### Step1

create a new directory to store the extension's files. 
Next, add a file called manifest.json, Every app needs a manifest, JSON-formatted file named manifest.json that describes the app and include the following code:

```markdown
{
  "name": "Hello Extensions",
  "description" : "Base Level Extension",
  "version": "1.0",
  "browser_action": {
    "default_popup": "hello.html",
    "default_icon": "hello_extensions.png"
  },
  "manifest_version": 2,
  "commands": {
    "_execute_browser_action": {
      "suggested_key": {
        "default": "Ctrl+Shift+F",
        "mac": "MacCtrl+Shift+F"
      },
      "description": "Opens hello.html"
    }
  }
}
```

### Step2

Get image for your app icon and save in same directory and then create a file titled hello.html:

```markdown
 <html>
    <body>
      <h1>Hello Extensions</h1>
    </body>
  </html>
```


### Step3

install the extension on your local machine.

```markdown
1.Navigate to chrome://extensions in your browser. You can also access this page by clicking on the Chrome menu on the top right side of the Omnibox, hovering over More Tools and selecting Extensions.

2.Check the box next to Developer Mode.

3.Click Load Unpacked Extension and select the directory for your "Hello Extensions" extension.
```
Congratulations! You can now launch your popup-based extension by clicking the app icon or by pressing Ctrl+Shift+F on your keyboard.



### Step4 

Web Store Hosting.

1. All extensions are distributed to users as a special ZIP file with a .crx suffix. Extensions hosted in the Chrome Web Store are uploaded through the Developer Dashboard as .zip files. The publishing process automatically converts the .zip into a .crx file.

2.There are three exceptions to the Chrome Web Store hosting rule:

2.1 [Extensions that are distributed through the enterprise policy](https://support.google.com/chrome/a/answer/187948?visit_id=637299903277586562-2444179625&rd=1).\
2.2 [Unpacked extension directories from a local machine while in developer mode](https://developer.chrome.com/extensions/getstarted#unpacked).\
2.3 [Linux installation](https://developer.chrome.com/extensions/linux_hosting).



