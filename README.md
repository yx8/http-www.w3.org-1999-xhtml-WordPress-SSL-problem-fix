If you just installed your SSL certificate on your WordPress website and fount out on the dashboard page the website url is marked as an insecured one. 

In most cases it's caused by this link "http://www.w3.org/1999/xhtml" on the dashboard page. This link is written as "http" instead of "https" in a lot of plugins which were developed a few years ago when SSL wasn't so popular. So it had to be written in "http".

If you want a fix to make the WordPress dashboard page secure again here is a solution. 

![1](https://github.com/yx8/http-www.w3.org-1999-xhtml-WordPress-SSL-problem-fix/blob/master/images/1.png?raw=true)

First is to use FTP tool to download everything of your WP website inside "/public_html" directory.

Then open up a text editor tool. 

![2](https://github.com/yx8/http-www.w3.org-1999-xhtml-WordPress-SSL-problem-fix/blob/master/images/2.png?raw=true)

Open the "Find in File" function, search for this string "http://www.w3.org/1999/xhtml" under the folder where you downloaded all you WP files. 

Let it search for a few seconds to two minutes. 

![3](https://github.com/yx8/http-www.w3.org-1999-xhtml-WordPress-SSL-problem-fix/blob/master/images/3.png?raw=true)

On the search results page, there are a lot of directories and codes contaioning the string you searched for.

Then we use the ftp tool to find the files in the directories we searched. Note here we only need to edit the files on the server not in local directory where you downloaded them. 

Replace all the "http://www.w3.org/1999/xhtml" strings into "https://www.w3.org/1999/xhtml", just add an "s" after http.

Note on the search result page, on the right side bar thumbnail, see the figure I put here, we only need to replace the strings in the red square section, in the blue aquare there are some other code written in js or whateve we don't need to replace the strings in there, otherwise it will be too much to do. 

After replaced all the "http://www.w3.org/1999/xhtml" strings, close all the WordPress Page in the browser, and reopen them again, then you will see the dashboard page is now marked as secure. And it is all fixed.

![4](https://github.com/yx8/http-www.w3.org-1999-xhtml-WordPress-SSL-problem-fix/blob/master/images/4.png?raw=true)

If you have a look the source code of the dashboard now you can see the string "http://www.w3.org/1999/xhtml" is now replaced in https.

Hope this solution is working for you. :)


