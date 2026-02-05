# zap_report_round1

ZAP by [Checkmarx](https://checkmarx.com/).


## Summary of Alerts

| Risk Level | Number of Alerts |
| --- | --- |
| High | 0 |
| Medium | 3 |
| Low | 4 |
| Informational | 1 |




## Insights

| Level | Reason | Site | Description | Statistic |
| --- | --- | --- | --- | --- |
| Low | Warning |  | ZAP warnings logged - see the zap.log file for details | 22    |
| Low | Exceeded High | http://localhost:8001 | Percentage of responses with status code 5xx | 53 % |
| Info | Informational | http://clients2.google.com | Percentage of responses with status code 2xx | 100 % |
| Info | Informational | http://clients2.google.com | Percentage of endpoints with content type application/json | 100 % |
| Info | Informational | http://clients2.google.com | Percentage of endpoints with method GET | 100 % |
| Info | Informational | http://clients2.google.com | Count of total endpoints | 1    |
| Info | Informational | http://localhost:8001 | Percentage of responses with status code 2xx | 17 % |
| Info | Informational | http://localhost:8001 | Percentage of responses with status code 3xx | 9 % |
| Info | Exceeded Low | http://localhost:8001 | Percentage of responses with status code 4xx | 19 % |
| Info | Informational | http://localhost:8001 | Percentage of endpoints with content type image/png | 5 % |
| Info | Informational | http://localhost:8001 | Percentage of endpoints with content type text/css | 5 % |
| Info | Informational | http://localhost:8001 | Percentage of endpoints with content type text/html | 17 % |
| Info | Informational | http://localhost:8001 | Percentage of endpoints with content type text/javascript | 11 % |
| Info | Informational | http://localhost:8001 | Percentage of endpoints with content type text/plain | 52 % |
| Info | Informational | http://localhost:8001 | Percentage of endpoints with method GET | 94 % |
| Info | Informational | http://localhost:8001 | Percentage of endpoints with method POST | 5 % |
| Info | Informational | http://localhost:8001 | Count of total endpoints | 17    |
| Info | Informational | http://localhost:8001 | Percentage of slow responses | 4 % |
| Info | Informational | https://accounts.google.com | Percentage of responses with status code 2xx | 100 % |
| Info | Informational | https://accounts.google.com | Percentage of endpoints with content type application/binary | 100 % |
| Info | Informational | https://accounts.google.com | Percentage of endpoints with method POST | 100 % |
| Info | Informational | https://accounts.google.com | Count of total endpoints | 1    |
| Info | Informational | https://android.clients.google.com | Percentage of responses with status code 2xx | 42 % |
| Info | Informational | https://android.clients.google.com | Percentage of responses with status code 3xx | 57 % |
| Info | Informational | https://android.clients.google.com | Percentage of endpoints with content type application/x-protobuffer | 33 % |
| Info | Informational | https://android.clients.google.com | Percentage of endpoints with content type text/plain | 66 % |
| Info | Informational | https://android.clients.google.com | Percentage of endpoints with method POST | 100 % |
| Info | Informational | https://android.clients.google.com | Count of total endpoints | 3    |
| Info | Informational | https://android.clients.google.com | Percentage of slow responses | 28 % |
| Info | Informational | https://content-autofill.googleapis.com | Percentage of responses with status code 2xx | 100 % |
| Info | Informational | https://content-autofill.googleapis.com | Percentage of endpoints with content type text/plain | 100 % |
| Info | Informational | https://content-autofill.googleapis.com | Percentage of endpoints with method GET | 100 % |
| Info | Informational | https://content-autofill.googleapis.com | Count of total endpoints | 1    |
| Info | Informational | https://optimizationguide-pa.googleapis.com | Percentage of responses with status code 2xx | 100 % |
| Info | Informational | https://optimizationguide-pa.googleapis.com | Percentage of endpoints with content type application/x-protobuf | 50 % |
| Info | Informational | https://optimizationguide-pa.googleapis.com | Percentage of endpoints with content type text/html | 50 % |
| Info | Informational | https://optimizationguide-pa.googleapis.com | Percentage of endpoints with method GET | 50 % |
| Info | Informational | https://optimizationguide-pa.googleapis.com | Percentage of endpoints with method POST | 50 % |
| Info | Informational | https://optimizationguide-pa.googleapis.com | Count of total endpoints | 2    |
| Info | Informational | https://optimizationguide-pa.googleapis.com | Percentage of slow responses | 60 % |
| Info | Informational | https://update.googleapis.com | Percentage of responses with status code 2xx | 100 % |
| Info | Informational | https://update.googleapis.com | Percentage of endpoints with content type application/json | 100 % |
| Info | Informational | https://update.googleapis.com | Percentage of endpoints with method POST | 100 % |
| Info | Informational | https://update.googleapis.com | Count of total endpoints | 1    |
| Info | Informational | https://www.google.com | Percentage of responses with status code 2xx | 100 % |
| Info | Informational | https://www.google.com | Percentage of endpoints with content type application/x-protobuffer | 100 % |
| Info | Informational | https://www.google.com | Percentage of endpoints with method GET | 100 % |
| Info | Informational | https://www.google.com | Count of total endpoints | 1    |
| Info | Informational | https://www.googleapis.com | Percentage of responses with status code 2xx | 100 % |
| Info | Informational | https://www.googleapis.com | Percentage of endpoints with content type application/json | 100 % |
| Info | Informational | https://www.googleapis.com | Percentage of endpoints with method POST | 100 % |
| Info | Informational | https://www.googleapis.com | Count of total endpoints | 1    |
| Info | Informational | https://www.googleapis.com | Percentage of slow responses | 100 % |




## Alerts

| Name | Risk Level | Number of Instances |
| --- | --- | --- |
| Absence of Anti-CSRF Tokens | Medium | 1 |
| Content Security Policy (CSP) Header Not Set | Medium | 5 |
| Missing Anti-clickjacking Header | Medium | 5 |
| Application Error Disclosure | Low | 1 |
| Strict-Transport-Security Header Not Set | Low | 8 |
| Timestamp Disclosure - Unix | Low | Systemic |
| X-Content-Type-Options Header Missing | Low | Systemic |
| Re-examine Cache-control Directives | Informational | 2 |




## Alert Detail



### [ Absence of Anti-CSRF Tokens ](https://www.zaproxy.org/docs/alerts/10202/)



##### Medium (Low)

### Description

No Anti-CSRF tokens were found in a HTML submission form.
A cross-site request forgery is an attack that involves forcing a victim to send an HTTP request to a target destination without their knowledge or intent in order to perform an action as the victim. The underlying cause is application functionality using predictable URL/form actions in a repeatable way. The nature of the attack is that CSRF exploits the trust that a web site has for a user. By contrast, cross-site scripting (XSS) exploits the trust that a user has for a web site. Like XSS, CSRF attacks are not necessarily cross-site, but they can be. Cross-site request forgery is also known as CSRF, XSRF, one-click attack, session riding, confused deputy, and sea surf.

CSRF attacks are effective in a number of situations, including:
    * The victim has an active session on the target site.
    * The victim is authenticated via HTTP auth on the target site.
    * The victim is on the same local network as the target site.

CSRF has primarily been used to perform an action against a target site using the victim's privileges, but recent techniques have been discovered to disclose information by gaining access to the response. The risk of information disclosure is dramatically increased when the target site is vulnerable to XSS, because XSS can be used as a platform for CSRF, allowing the attack to operate within the bounds of the same-origin policy.

* URL: http://localhost:8001/register
  * Node Name: `http://localhost:8001/register`
  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `<form action="/register" method="POST">`
  * Other Info: `No known Anti-CSRF token [anticsrf, CSRFToken, __RequestVerificationToken, csrfmiddlewaretoken, authenticity_token, OWASP_CSRFTOKEN, anoncsrf, csrf_token, _csrf, _csrfSecret, __csrf_magic, CSRF, _token, _csrf_token, _csrfToken] was found in the following HTML form: [Form 1: "birthdate" "password" "username" ].`


Instances: 1

### Solution

Phase: Architecture and Design
Use a vetted library or framework that does not allow this weakness to occur or provides constructs that make this weakness easier to avoid.
For example, use anti-CSRF packages such as the OWASP CSRFGuard.

Phase: Implementation
Ensure that your application is free of cross-site scripting issues, because most CSRF defenses can be bypassed using attacker-controlled script.

Phase: Architecture and Design
Generate a unique nonce for each form, place the nonce into the form, and verify the nonce upon receipt of the form. Be sure that the nonce is not predictable (CWE-330).
Note that this can be bypassed using XSS.

Identify especially dangerous operations. When the user performs a dangerous operation, send a separate confirmation request to ensure that the user intended to perform that operation.
Note that this can be bypassed using XSS.

Use the ESAPI Session Management control.
This control includes a component for CSRF.

Do not use the GET method for any request that triggers a state change.

Phase: Implementation
Check the HTTP Referer header to see if the request originated from an expected page. This could break legitimate functionality, because users or proxies may have disabled sending the Referer for privacy reasons.

### Reference


* [ https://cheatsheetseries.owasp.org/cheatsheets/Cross-Site_Request_Forgery_Prevention_Cheat_Sheet.html ](https://cheatsheetseries.owasp.org/cheatsheets/Cross-Site_Request_Forgery_Prevention_Cheat_Sheet.html)
* [ https://cwe.mitre.org/data/definitions/352.html ](https://cwe.mitre.org/data/definitions/352.html)


#### CWE Id: [ 352 ](https://cwe.mitre.org/data/definitions/352.html)


#### WASC Id: 9

#### Source ID: 3

### [ Content Security Policy (CSP) Header Not Set ](https://www.zaproxy.org/docs/alerts/10038/)



##### Medium (High)

### Description

Content Security Policy (CSP) is an added layer of security that helps to detect and mitigate certain types of attacks, including Cross Site Scripting (XSS) and data injection attacks. These attacks are used for everything from data theft to site defacement or distribution of malware. CSP provides a set of standard HTTP headers that allow website owners to declare approved sources of content that browsers should be allowed to load on that page — covered types are JavaScript, CSS, HTML frames, fonts, images and embeddable objects such as Java applets, ActiveX, audio and video files.

* URL: http://localhost:8001
  * Node Name: `http://localhost:8001`
  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: ``
  * Other Info: ``
* URL: http://localhost:8001/
  * Node Name: `http://localhost:8001/`
  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: ``
  * Other Info: ``
* URL: http://localhost:8001/register
  * Node Name: `http://localhost:8001/register`
  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: ``
  * Other Info: ``
* URL: http://localhost:8001/static/footer.html
  * Node Name: `http://localhost:8001/static/footer.html`
  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: ``
  * Other Info: ``
* URL: https://optimizationguide-pa.googleapis.com/downloads%3Fname=1767628897&target=OPTIMIZATION_TARGET_NOTIFICATION_PERMISSION_PREDICTIONS
  * Node Name: `https://optimizationguide-pa.googleapis.com/downloads (name,target)`
  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: ``
  * Other Info: ``


Instances: 5

### Solution

Ensure that your web server, application server, load balancer, etc. is configured to set the Content-Security-Policy header.

### Reference


* [ https://developer.mozilla.org/en-US/docs/Web/HTTP/Guides/CSP ](https://developer.mozilla.org/en-US/docs/Web/HTTP/Guides/CSP)
* [ https://cheatsheetseries.owasp.org/cheatsheets/Content_Security_Policy_Cheat_Sheet.html ](https://cheatsheetseries.owasp.org/cheatsheets/Content_Security_Policy_Cheat_Sheet.html)
* [ https://www.w3.org/TR/CSP/ ](https://www.w3.org/TR/CSP/)
* [ https://w3c.github.io/webappsec-csp/ ](https://w3c.github.io/webappsec-csp/)
* [ https://web.dev/articles/csp ](https://web.dev/articles/csp)
* [ https://caniuse.com/#feat=contentsecuritypolicy ](https://caniuse.com/#feat=contentsecuritypolicy)
* [ https://content-security-policy.com/ ](https://content-security-policy.com/)


#### CWE Id: [ 693 ](https://cwe.mitre.org/data/definitions/693.html)


#### WASC Id: 15

#### Source ID: 3

### [ Missing Anti-clickjacking Header ](https://www.zaproxy.org/docs/alerts/10020/)



##### Medium (Medium)

### Description

The response does not protect against 'ClickJacking' attacks. It should include either Content-Security-Policy with 'frame-ancestors' directive or X-Frame-Options.

* URL: http://localhost:8001
  * Node Name: `http://localhost:8001`
  * Method: `GET`
  * Parameter: `x-frame-options`
  * Attack: ``
  * Evidence: ``
  * Other Info: ``
* URL: http://localhost:8001/
  * Node Name: `http://localhost:8001/`
  * Method: `GET`
  * Parameter: `x-frame-options`
  * Attack: ``
  * Evidence: ``
  * Other Info: ``
* URL: http://localhost:8001/register
  * Node Name: `http://localhost:8001/register`
  * Method: `GET`
  * Parameter: `x-frame-options`
  * Attack: ``
  * Evidence: ``
  * Other Info: ``
* URL: http://localhost:8001/static/footer.html
  * Node Name: `http://localhost:8001/static/footer.html`
  * Method: `GET`
  * Parameter: `x-frame-options`
  * Attack: ``
  * Evidence: ``
  * Other Info: ``
* URL: https://optimizationguide-pa.googleapis.com/downloads%3Fname=1767628897&target=OPTIMIZATION_TARGET_NOTIFICATION_PERMISSION_PREDICTIONS
  * Node Name: `https://optimizationguide-pa.googleapis.com/downloads (name,target)`
  * Method: `GET`
  * Parameter: `x-frame-options`
  * Attack: ``
  * Evidence: ``
  * Other Info: ``


Instances: 5

### Solution

Modern Web browsers support the Content-Security-Policy and X-Frame-Options HTTP headers. Ensure one of them is set on all web pages returned by your site/app.
If you expect the page to be framed only by pages on your server (e.g. it's part of a FRAMESET) then you'll want to use SAMEORIGIN, otherwise if you never expect the page to be framed, you should use DENY. Alternatively consider implementing Content Security Policy's "frame-ancestors" directive.

### Reference


* [ https://developer.mozilla.org/en-US/docs/Web/HTTP/Reference/Headers/X-Frame-Options ](https://developer.mozilla.org/en-US/docs/Web/HTTP/Reference/Headers/X-Frame-Options)


#### CWE Id: [ 1021 ](https://cwe.mitre.org/data/definitions/1021.html)


#### WASC Id: 15

#### Source ID: 3

### [ Application Error Disclosure ](https://www.zaproxy.org/docs/alerts/90022/)



##### Low (Medium)

### Description

This page contains an error/warning message that may disclose sensitive information like the location of the file that produced the unhandled exception. This information can be used to launch further attacks against the web application. The alert could be a false positive if the error message is found inside a documentation page.

* URL: http://localhost:8001/register
  * Node Name: `http://localhost:8001/register ()(birthdate,password,role,username)`
  * Method: `POST`
  * Parameter: ``
  * Attack: ``
  * Evidence: `HTTP/1.1 500 Internal Server Error`
  * Other Info: ``


Instances: 1

### Solution

Review the source code of this page. Implement custom error pages. Consider implementing a mechanism to provide a unique error reference/identifier to the client (browser) while logging the details on the server side and not exposing them to the user.

### Reference



#### CWE Id: [ 550 ](https://cwe.mitre.org/data/definitions/550.html)


#### WASC Id: 13

#### Source ID: 3

### [ Strict-Transport-Security Header Not Set ](https://www.zaproxy.org/docs/alerts/10035/)



##### Low (High)

### Description

HTTP Strict Transport Security (HSTS) is a web security policy mechanism whereby a web server declares that complying user agents (such as a web browser) are to interact with it using only secure HTTPS connections (i.e. HTTP layered over TLS/SSL). HSTS is an IETF standards track protocol and is specified in RFC 6797.

* URL: https://content-autofill.googleapis.com/v1/pages/ChVDaHJvbWUvMTQ0LjAuNzU1OS4xMTISLgkpKaFsFNIqrBIFDVNVgbUSBQ3OQUx6EgUNaPg5uhIFDV0anrAhvddWjLD5fZIYt6nKAQ==%3Falt=proto
  * Node Name: `https://content-autofill.googleapis.com/v1/pages/ChVDaHJvbWUvMTQ0LjAuNzU1OS4xMTISLgkpKaFsFNIqrBIFDVNVgbUSBQ3OQUx6EgUNaPg5uhIFDV0anrAhvddWjLD5fZIYt6nKAQ== (alt)`
  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: ``
  * Other Info: ``
* URL: https://optimizationguide-pa.googleapis.com/downloads%3Fname=1767628897&target=OPTIMIZATION_TARGET_NOTIFICATION_PERMISSION_PREDICTIONS
  * Node Name: `https://optimizationguide-pa.googleapis.com/downloads (name,target)`
  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: ``
  * Other Info: ``
* URL: https://android.clients.google.com/c2dm/register3
  * Node Name: `https://android.clients.google.com/c2dm/register3 ()(X-scope,X-subtype,app,appid,device,gmsv,scope,sender,ttl)`
  * Method: `POST`
  * Parameter: ``
  * Attack: ``
  * Evidence: ``
  * Other Info: ``
* URL: https://android.clients.google.com/c2dm/register3
  * Node Name: `https://android.clients.google.com/c2dm/register3 ()(app,device,sender)`
  * Method: `POST`
  * Parameter: ``
  * Attack: ``
  * Evidence: ``
  * Other Info: ``
* URL: https://android.clients.google.com/checkin
  * Node Name: `https://android.clients.google.com/checkin ()( *1-da39a3ee5e6b4b0d3255bfef95601890af...)`
  * Method: `POST`
  * Parameter: ``
  * Attack: ``
  * Evidence: ``
  * Other Info: ``
* URL: https://optimizationguide-pa.googleapis.com/v1:GetModels%3Fkey=AIzaSyA2KlwBX3mkFo30om9LUFYQhpqLoa_BNhE
  * Node Name: `https://optimizationguide-pa.googleapis.com/v1:GetModels (key)(
 
n	 2h
atype.googleapis.com/goog...)`
  * Method: `POST`
  * Parameter: ``
  * Attack: ``
  * Evidence: ``
  * Other Info: ``
* URL: https://update.googleapis.com/service/update2/json%3Fcup2key=15:owJjYDXS3L_9441LAq8AF1F6WviC02IlEfIw9WxOmOA&cup2hreq=47e135c0444cee1a99ed935cfe826cab830b3d1675a0eb88132449e596bcb46b
  * Node Name: `https://update.googleapis.com/service/update2/json (cup2hreq,cup2key)({request:{@os,@updater,acceptformat,apps:[{appid,brand,enabled,lang,ping:{r},updatecheck:{},version}..,{accept_locale,appid,brand,enabled,lang,ping:{r},updatecheck:{},version},{appid,brand,enabled,lang,ping:{r},updatecheck:{},version}..],arch,dedup,domainjoined,hw:{avx,physmemory,sse,sse2,sse3,sse41,sse42,ssse3},ismachine,os:{arch,platform,version},prodversion,protocol,requestid,sessionid,updaters:{autoupdatecheckenabled,ismachine,lastchecked,laststarted,name,updatepolicy,version},updaterversion}})`
  * Method: `POST`
  * Parameter: ``
  * Attack: ``
  * Evidence: ``
  * Other Info: ``
* URL: https://www.googleapis.com/chromewebstore/v1.1/items/verify
  * Node Name: `https://www.googleapis.com/chromewebstore/v1.1/items/verify ()({hash,ids:[],protocol_version})`
  * Method: `POST`
  * Parameter: ``
  * Attack: ``
  * Evidence: ``
  * Other Info: ``


Instances: 8

### Solution

Ensure that your web server, application server, load balancer, etc. is configured to enforce Strict-Transport-Security.

### Reference


* [ https://cheatsheetseries.owasp.org/cheatsheets/HTTP_Strict_Transport_Security_Cheat_Sheet.html ](https://cheatsheetseries.owasp.org/cheatsheets/HTTP_Strict_Transport_Security_Cheat_Sheet.html)
* [ https://owasp.org/www-community/Security_Headers ](https://owasp.org/www-community/Security_Headers)
* [ https://en.wikipedia.org/wiki/HTTP_Strict_Transport_Security ](https://en.wikipedia.org/wiki/HTTP_Strict_Transport_Security)
* [ https://caniuse.com/stricttransportsecurity ](https://caniuse.com/stricttransportsecurity)
* [ https://datatracker.ietf.org/doc/html/rfc6797 ](https://datatracker.ietf.org/doc/html/rfc6797)


#### CWE Id: [ 319 ](https://cwe.mitre.org/data/definitions/319.html)


#### WASC Id: 15

#### Source ID: 3

### [ Timestamp Disclosure - Unix ](https://www.zaproxy.org/docs/alerts/10096/)



##### Low (Low)

### Description

A timestamp was disclosed by the application/web server. - Unix

* URL: https://optimizationguide-pa.googleapis.com/v1:GetModels%3Fkey=AIzaSyA2KlwBX3mkFo30om9LUFYQhpqLoa_BNhE
  * Node Name: `https://optimizationguide-pa.googleapis.com/v1:GetModels (key)(
 
n	 2h
atype.googleapis.com/goog...)`
  * Method: `POST`
  * Parameter: ``
  * Attack: ``
  * Evidence: `1673999601`
  * Other Info: `1673999601, which evaluates to: 2023-01-18 01:53:21.`
* URL: https://optimizationguide-pa.googleapis.com/v1:GetModels%3Fkey=AIzaSyA2KlwBX3mkFo30om9LUFYQhpqLoa_BNhE
  * Node Name: `https://optimizationguide-pa.googleapis.com/v1:GetModels (key)(
 
n	 2h
atype.googleapis.com/goog...)`
  * Method: `POST`
  * Parameter: ``
  * Attack: ``
  * Evidence: `1679317318`
  * Other Info: `1679317318, which evaluates to: 2023-03-20 15:01:58.`
* URL: https://optimizationguide-pa.googleapis.com/v1:GetModels%3Fkey=AIzaSyA2KlwBX3mkFo30om9LUFYQhpqLoa_BNhE
  * Node Name: `https://optimizationguide-pa.googleapis.com/v1:GetModels (key)(
 
n	 2h
atype.googleapis.com/goog...)`
  * Method: `POST`
  * Parameter: ``
  * Attack: ``
  * Evidence: `1728324084`
  * Other Info: `1728324084, which evaluates to: 2024-10-07 21:01:24.`
* URL: https://optimizationguide-pa.googleapis.com/v1:GetModels%3Fkey=AIzaSyA2KlwBX3mkFo30om9LUFYQhpqLoa_BNhE
  * Node Name: `https://optimizationguide-pa.googleapis.com/v1:GetModels (key)(
 
n	 2h
atype.googleapis.com/goog...)`
  * Method: `POST`
  * Parameter: ``
  * Attack: ``
  * Evidence: `1745311339`
  * Other Info: `1745311339, which evaluates to: 2025-04-22 11:42:19.`
* URL: https://optimizationguide-pa.googleapis.com/v1:GetModels%3Fkey=AIzaSyA2KlwBX3mkFo30om9LUFYQhpqLoa_BNhE
  * Node Name: `https://optimizationguide-pa.googleapis.com/v1:GetModels (key)(
 
n	 2h
atype.googleapis.com/goog...)`
  * Method: `POST`
  * Parameter: ``
  * Attack: ``
  * Evidence: `1767628897`
  * Other Info: `1767628897, which evaluates to: 2026-01-05 18:01:37.`

Instances: Systemic


### Solution

Manually confirm that the timestamp data is not sensitive, and that the data cannot be aggregated to disclose exploitable patterns.

### Reference


* [ https://cwe.mitre.org/data/definitions/200.html ](https://cwe.mitre.org/data/definitions/200.html)


#### CWE Id: [ 497 ](https://cwe.mitre.org/data/definitions/497.html)


#### WASC Id: 13

#### Source ID: 3

### [ X-Content-Type-Options Header Missing ](https://www.zaproxy.org/docs/alerts/10021/)



##### Low (Medium)

### Description

The Anti-MIME-Sniffing header X-Content-Type-Options was not set to 'nosniff'. This allows older versions of Internet Explorer and Chrome to perform MIME-sniffing on the response body, potentially causing the response body to be interpreted and displayed as a content type other than the declared content type. Current (early 2014) and legacy versions of Firefox will use the declared content type (if one is set), rather than performing MIME-sniffing.

* URL: http://localhost:8001/
  * Node Name: `http://localhost:8001/`
  * Method: `GET`
  * Parameter: `x-content-type-options`
  * Attack: ``
  * Evidence: ``
  * Other Info: `This issue still applies to error type pages (401, 403, 500, etc.) as those pages are often still affected by injection issues, in which case there is still concern for browsers sniffing pages away from their actual content type.
At "High" threshold this scan rule will not alert on client or server error responses.`
* URL: http://localhost:8001/static/footer.html
  * Node Name: `http://localhost:8001/static/footer.html`
  * Method: `GET`
  * Parameter: `x-content-type-options`
  * Attack: ``
  * Evidence: ``
  * Other Info: `This issue still applies to error type pages (401, 403, 500, etc.) as those pages are often still affected by injection issues, in which case there is still concern for browsers sniffing pages away from their actual content type.
At "High" threshold this scan rule will not alert on client or server error responses.`
* URL: http://localhost:8001/static/footer.js
  * Node Name: `http://localhost:8001/static/footer.js`
  * Method: `GET`
  * Parameter: `x-content-type-options`
  * Attack: ``
  * Evidence: ``
  * Other Info: `This issue still applies to error type pages (401, 403, 500, etc.) as those pages are often still affected by injection issues, in which case there is still concern for browsers sniffing pages away from their actual content type.
At "High" threshold this scan rule will not alert on client or server error responses.`
* URL: http://localhost:8001/static/index.js
  * Node Name: `http://localhost:8001/static/index.js`
  * Method: `GET`
  * Parameter: `x-content-type-options`
  * Attack: ``
  * Evidence: ``
  * Other Info: `This issue still applies to error type pages (401, 403, 500, etc.) as those pages are often still affected by injection issues, in which case there is still concern for browsers sniffing pages away from their actual content type.
At "High" threshold this scan rule will not alert on client or server error responses.`
* URL: http://localhost:8001/static/tailwind.css
  * Node Name: `http://localhost:8001/static/tailwind.css`
  * Method: `GET`
  * Parameter: `x-content-type-options`
  * Attack: ``
  * Evidence: ``
  * Other Info: `This issue still applies to error type pages (401, 403, 500, etc.) as those pages are often still affected by injection issues, in which case there is still concern for browsers sniffing pages away from their actual content type.
At "High" threshold this scan rule will not alert on client or server error responses.`
* URL: https://optimizationguide-pa.googleapis.com/downloads%3Fname=1767628897&target=OPTIMIZATION_TARGET_NOTIFICATION_PERMISSION_PREDICTIONS
  * Node Name: `https://optimizationguide-pa.googleapis.com/downloads (name,target)`
  * Method: `GET`
  * Parameter: `x-content-type-options`
  * Attack: ``
  * Evidence: ``
  * Other Info: `This issue still applies to error type pages (401, 403, 500, etc.) as those pages are often still affected by injection issues, in which case there is still concern for browsers sniffing pages away from their actual content type.
At "High" threshold this scan rule will not alert on client or server error responses.`

Instances: Systemic


### Solution

Ensure that the application/web server sets the Content-Type header appropriately, and that it sets the X-Content-Type-Options header to 'nosniff' for all web pages.
If possible, ensure that the end user uses a standards-compliant and modern web browser that does not perform MIME-sniffing at all, or that can be directed by the web application/web server to not perform MIME-sniffing.

### Reference


* [ https://learn.microsoft.com/en-us/previous-versions/windows/internet-explorer/ie-developer/compatibility/gg622941(v=vs.85) ](https://learn.microsoft.com/en-us/previous-versions/windows/internet-explorer/ie-developer/compatibility/gg622941(v=vs.85))
* [ https://owasp.org/www-community/Security_Headers ](https://owasp.org/www-community/Security_Headers)


#### CWE Id: [ 693 ](https://cwe.mitre.org/data/definitions/693.html)


#### WASC Id: 15

#### Source ID: 3

### [ Re-examine Cache-control Directives ](https://www.zaproxy.org/docs/alerts/10015/)



##### Informational (Low)

### Description

The cache-control header has not been set properly or is missing, allowing the browser and proxies to cache content. For static assets like css, js, or image files this might be intended, however, the resources should be reviewed to ensure that no sensitive content will be cached.

* URL: https://content-autofill.googleapis.com/v1/pages/ChVDaHJvbWUvMTQ0LjAuNzU1OS4xMTISLgkpKaFsFNIqrBIFDVNVgbUSBQ3OQUx6EgUNaPg5uhIFDV0anrAhvddWjLD5fZIYt6nKAQ==%3Falt=proto
  * Node Name: `https://content-autofill.googleapis.com/v1/pages/ChVDaHJvbWUvMTQ0LjAuNzU1OS4xMTISLgkpKaFsFNIqrBIFDVNVgbUSBQ3OQUx6EgUNaPg5uhIFDV0anrAhvddWjLD5fZIYt6nKAQ== (alt)`
  * Method: `GET`
  * Parameter: `cache-control`
  * Attack: ``
  * Evidence: `private,max-age=604800`
  * Other Info: ``
* URL: https://optimizationguide-pa.googleapis.com/downloads%3Fname=1767628897&target=OPTIMIZATION_TARGET_NOTIFICATION_PERMISSION_PREDICTIONS
  * Node Name: `https://optimizationguide-pa.googleapis.com/downloads (name,target)`
  * Method: `GET`
  * Parameter: `cache-control`
  * Attack: ``
  * Evidence: `public, max-age=86400`
  * Other Info: ``


Instances: 2

### Solution

For secure content, ensure the cache-control HTTP header is set with "no-cache, no-store, must-revalidate". If an asset should be cached consider setting the directives "public, max-age, immutable".

### Reference


* [ https://cheatsheetseries.owasp.org/cheatsheets/Session_Management_Cheat_Sheet.html#web-content-caching ](https://cheatsheetseries.owasp.org/cheatsheets/Session_Management_Cheat_Sheet.html#web-content-caching)
* [ https://developer.mozilla.org/en-US/docs/Web/HTTP/Reference/Headers/Cache-Control ](https://developer.mozilla.org/en-US/docs/Web/HTTP/Reference/Headers/Cache-Control)
* [ https://grayduck.mn/2021/09/13/cache-control-recommendations/ ](https://grayduck.mn/2021/09/13/cache-control-recommendations/)


#### CWE Id: [ 525 ](https://cwe.mitre.org/data/definitions/525.html)


#### WASC Id: 13

#### Source ID: 3


