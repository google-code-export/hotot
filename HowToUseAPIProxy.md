

## 1. Supported API Proxies ##

API proxy was, is and will be commonly and widely used by most users from China behind the firewall.

> <b>What is API proxy?</b>

> Contributors outside mainland China always be perplexed by the ambiguity of API proxy. We do know API is the abbreviation of Application Program Interface and Proxy is a redirect method. So the combination of them means here we create a program functions rebinding an API call to twitter.com, that is blocked by Bin Xing Fung and his great firewall, to our web based application and calling to twitter.com from it. this two way program works like a proxy, but it does not re-transfer the normal http request but twitter API calls.

> During the re-transfer, calls can be modified by our application or not. if they are, Override mode outcomes; if not, here comes Transparent Mode.

Hotot has been tested with these two API proxies.

  * [Twip](http://code.google.com/p/twip) (both 3.x and 4.x)
  * [Gtap](http://code.google.com/p/gtap/)

## 2. Using Twip ##

Twip is a PHP-based API proxy. The latest version(Twip4) works in two different modes, T(transparent) mode and O(override) mode.

Hotot supports both of them recently.

### 2.1 Using T mode of Twip (Recommend) ###
  1. Setup your Twip (visit the [wiki of Twip](http://code.google.com/p/twip/wiki/ForUser) for more info);
  1. Launch Hotot for the 1st time, create a Twitter profile, but <b>do not get oauth token</b>;
  1. Go "Preferences"->"Networks"->API Settings;
  1. Fill text entry "API Base" with your API\_BASE\_URL/t/(<b>take care of the ending backlash.</b>)
  1. Make sure you have unchecked "Same signing API base"
  1. Make sure the URL in text entry "Signing API Base" is "https://api.twitter.com/1/"
  1. Fill text entry "OAuth Base" with your API\_BASE\_URL/t/oauth/
  1. Make sure you have unchecked "Same signing OAuth base"
  1. Make sure the URL in text entry "Signing OAuth Base" is "https://api.twitter.com/oauth/"
  1. Press OK to save your changes.
  1. Sign out, use OAuth to sign in.
  1. Copy the url in the textbox, open it in your browser, input your twitter username and password, authorize our application, click "okay", returns a string, now input it in Hotot.
  1. Now success! Congrats and enjoy yourself.

### 2.2 Using O mode of Twip ###
  1. Setup your Twip (visit the [Wiki of Twip](http://code.google.com/p/twip/wiki/ForUser) for more info);
  1. Launch Hotot, Create a identi.ca profile and go "Preferences"->"Networks"->API Settings;
  1. Fill text entry "API Base" with your API\_BASE\_URL/o/Twitter\_Username/Random\_String\_Generated\_By\_TWIP4/
  1. Make sure you have checked "Same signing API base"
  1. Press OK to save your changes.
  1. Sign out, use basic auth to sign in.


**Notice** that the username or password is ignored when using o mode,so you can input anything.

**Notice** that if you are using twip (3.x), the password is the TWIP password, not your twitter password.

_Tutorial below is NOT reviewed and tested with the last version, so its availability is unknown._

## 3. Using Gtap ##
Gtap is a simple solution running on Google App Engine which can proxy the HTTP request to twitter's official REST API URL.

  1. Setup your Gtap (visit the [wiki of Gtap](http://code.google.com/p/gtap/w/list) for more info);
  1. Launch Hotot, Create a identi.ca profile go "Preferences"->"Networks"->API Settings;
  1. Fill text entry "API Base" with your API\_BASE\_URL
  1. Make sure you have checked "Same signing API base"
  1. Press OK to save your changes.
  1. Sign out, use basic auth to sign in.

Notice that the password is the GTAP password, not your twitter password.

GOOD LUCK！


Marguerite.