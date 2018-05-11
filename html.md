What is the difference between sessionStorage, localStorage, and Cookies? Cookies are primarily for server-side reading (can also be read on client-side), localStorage and sessionStorage can only be read on client-side.
- localStorage: 
    - Available size is 5 MB which is considerably more space than a typical 4 KB cookie
    - Data is not sent back to server for every HTTP request
    - The data stored in localStorage persists until explicitly deleted.
    - It works on same-origin policy. So, data stored will only be available on the same origin
- Cookies
    - Can set the expiration time
    - 4KB limit
    - Data is sent back to the server for every HTTP request. Increasing the amount of traffic between client and server.
    - Cookies are primarily for server side reading
- sessionStorage
    - Changes are only available per window. Changes made are saved and available for the current page as well as future visits to the site on the same window. Once the window is closed, the storage is deleted

Difference between <script>, <script defer>, and <script async>?
- <script>:
    - Parsing of the HTML code pauses while the script is executing. 
- <script defer>
    - Delays script execution until the HTML parser has finished. Guarantees that the DOM will be available for your script
- <script async>
    - HTMl parsing may continue and the script will be executed as soon as it’s ready

Why is it a good idea to position CSS <link> between <head></head>?
- This prevents the information on the page from showing up unsettled while the rest of the page is being parsed.

Why is it a good idea to position <script>just before </body>?
- Javascript blocks rendering by default, and the DOM and CSSOM construction can also be delayed

What is progressive rendering?
- This is separating the HTML into various chunks. Where you might load one component first and then load another component after the initial one finishes loading.