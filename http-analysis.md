********************

https://discord.com/

********************

Name: discord.com 
Type: HTML document
Request Method: GET
Request URL: https://discord.com/
Response Status Code: 200 OK
Time: 66.01ms

Response Header 1: Cache-Control, no-cache - 
It may cache a response, but has to make a request to an origin server.
Response Header 2: NEL, {"report_to":"cf-nel","success_fraction":0.0,"max_age":604800} - 
Network Error Logging. report_to cf-nel tells where it's reporting to if there is a report needed. success_fraction 0.0 means there were no errors to report. max_age means this will be remembered for 604800 seconds or 7 days. 

********************

Name: 664754815450cb39bca27b05_Smoke.gif
Type: GIF
Request Method: GET
Request URL: https://cdn.prod.website-files.com/6257adef93867e50d84d30e2/664754815450cb39bca27b05_Smoke.gif
Response Status Code: 200 OK
Time: 850.46ms

Response Header 1: Content-Type, image/gif - 
the image is a gif! 
Response Header 2: Content-Length, 129478 - 
The exact size of the message body in bytes.

********************

Name: discord-2022.shared.182faf9a3.min.css
Type: stylesheet
Request Method: GET
Request URL: https://cdn.prod.website-files.com/6257adef93867e50d84d30e2/css/discord-2022.shared.182faf9a3.min.css
Response Status Code: 200 OK
Time: 160.46ms

Response Header 1: access-control-max-age, 3000 - 
How long in seconds the results of a "preflight request" can be cached. 
Response Header 2: Server, cloudflare - 
The server handling these requests is Cloudfare.

At first, I was surprised that the Smoke.gif (850.46ms) took much longer to queue than the other two. It's a simple gif that hardly has much weight to it. However, upon more thought I realized that the Discord HTML document (66.01ms) and the CSS file (160.46ms) were quite literally the foundation of the webpage and consisted of only characters, text-based information easily read and delivered. The GIF on the other hand is a bunch of images strewn together that has to be downloaded and processed, so of course it took longer to load. It's not nearly as important as the HTML document and CSS file, as it's only decoration. It needs more processing because of that and is further back on the queue at 800.5ms. 

All three requests had the status code of 200 OK, though I don't doubt there were other status codes on the list. But because the site is mostly a display site and the only interaction would potentially be cache and a login-button, I doubt it'd be sending much information to the server anyway. The 200 OKs show that the content was successfully taken from the server to display to the user. 

Headers gave information on how to handle resources, like the Content-Type: image/gif header told the browser that the response was a GIF. And the Cache-Control: no-cache asked the server for a cached copy instead of using one without permission.



