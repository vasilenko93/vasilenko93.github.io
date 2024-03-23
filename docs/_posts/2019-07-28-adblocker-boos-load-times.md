---
layout: post
title:  "Personal Study: Ad blockers will greatly boost page loads"
date:   2019-07-28 00:00:00 -0700
categories: technology ad-blockers browsers internet
---
It will not be a surprise to most internet users that adblockers not only block ads and block malware (also known as [adware](https://www.malwarebytes.com/adware/)) that may be inside the ads, but will also greatly boost page load times and cut down on bandwidth usage. In this hardly scientific personal study of mine I will go to a few technology news sites with and without an adblocker to determine how much time, bandwidth, and requests I save.


#### My setup:
Windows 10 Home 64-bit
Google Chrome Version 75.0.3770.142 (Official Build) (64-bit)
Adblocker: https://getadblock.com/

#### Methodology
The tool I used to gather information is Google Chrome’s Developer Tools which gave me useful statistics like total HTTP requests made, DOM load time (the content of the site showed up), total load time (the loading spinner stopped spinning), when background threads stopped loading, bandwidth used over the wire, and total content loaded. To avoid getting content cached from previous loads I used Google Chrome’s “Empty Cache and Hard Reload” which shows up if the page is open with Developer Tools by clicking F12 and you right-click the reload icon. For me, the page is considered “loaded” when the loading spinner stops spinning for Google Chrome. For each website I performed the following steps:

1. Open Develop Tools on the current Tab,
2. Disable my adblocker,
3. Navigate to the webpage URL, do not wait for the page to load,
4. Empty Cache and Hard Reload,
5. Wait for the page to load,
6. Screenshot the Developer Tools statistics,
7. Enable the adblocker,
8. Empty Cache and Hard Reload,
9. Wait for the page to load,
10. Screenshot the Developer Tools statistics.

## Engadget.com

![Engadget.com without ad-block and with ad-block](/assets/img/engadget.com_no_ad_blocker.png)

### Results for Engadget.com:

- **Total Requests**: we notice a sudden drop in total HTTP requests, almost a 50% reduction. This means fewer DNS lookups, less routing, and less home network congestion. **<font color="green">49.5% decrease</font>**.
- **Transferred**: we notice a full Megabyte reduction of internet bandwidth usage, it may not seem much but we visit thousands of webpages a day so those Megabytes will add up. **<font color="green">30.5% decrease</font>**.
- **Resources**: We noticed that the 1 MB of less bandwidth also correlated with fewer resources used (some content is compressed over transit and gets decompressed by your computer), using an adblocker means decreased RAM usage for this webpage. **<font color="green">31.5% decrease</font>**.
- **DOMContentLoaded**: This shows when the HTML and CSS of the webpage got loaded and rendered, an ad blocker will not affect this figure. The slight variation between with adblocker and without adblocker I will attribute to decreased internet speeds at the moment of the page reload as I have wireless. **<font color="red">9.3% increase</font>**.
- **Load**: This is the time after the page is fully loaded, or in my definition, the loading spinner stops spinning. After this time I consider a webpage is ready to be used. **<font color="green">47% decrease</font>**.
- **Finish**: I mention this column last because it is the most interesting. This represents background nonblocking asynchronous objects and requests finishing. The website is completely usable while these are happening so this number can be ignored for most practical purposes. For Engadget.com this happened much longer after the page finished loading because, as you can see from the pixel.gif requests in the no adblocker picture, requests are being sent to data collectors about the user after the page is loaded. Everything from mouse movement to cursor position to window scrolling. I cannot confirm that is what Engadget.com is sending but that is my guess. Too much background requests lead to more HTTP requests made and more bandwidth usage. **<font color="green">87% decrease</font>**, and counting.
 

## gizmodo.com

![gizmodo.com without ad-block and with ad-block](/assets/img/gizmodo.com_no_ad_blocker.png)

Results for gizmodo.com:

- **Total Requests**: <font color="green">51.7% decrease</font>.
- **Transferred**: <font color="green">45.7% decrease</font>.
- **Resources**:  <font color="green">54% decrease</font>.
- **DOMContentLoaded**: <font color="red">0.5% increase</font>.
- **Load**:  <font color="green">10% decrease</font>.
- **Finish**: <font color="green">82% decrease</font>, and counting.

## Slashdot.org

![slashdot.org without ad-block and with ad-block](/assets/img/slashdot.org_no_ad_blocker.png)

Results for slashdot.org:

- **Total Requests**: <font color="green">73.7% decrease</font>.
- **Transferred**: <font color="green">27.2% decrease</font>.
- **Resources**:  <font color="green">64.4% decrease</font>.
- **DOMContentLoaded**: <font color="green">1.1% decrease</font>.
- **Load**: <font color="green">67.3% decrease</font>.
- **Finish**: <font color="green">89.7% decrease</font>, and counting.

## Techcrunch.com

![techcrunch.com without ad-block and with ad-block](/assets/img/techcrunch.com_no_ad_blocker.png)

Results for TechCrunch.com:

- **Total Requests**: <font color="green">69.7% decrease</font>.
- **Transferred**: <font color="green">30.3% decrease</font>.
- **Resources**:  <font color="green">30.4% decrease</font>.
- **DOMContentLoaded**: <font color="green">7.6% decrease</font>.
- **Load**: <font color="green">90.5% decrease</font>.
- **Finish**: <font color="green">92.9% decrease</font>, and counting.

## Conclusion
It is clear that an adblocker will not only protect you from malware and hide annoying advertisements from your eyes, it will also make your webpages load faster and use less of your internet bandwidth. A win for everyone except the website owner.





