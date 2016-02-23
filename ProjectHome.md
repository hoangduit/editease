# editEase - no fuss, no database, no worries #

## May 2012 Update ##
Due to other commitments, I unfortunately have to close this project.  The downloads have been deprecated, and are only online for historical reasons.


## December 2011 Update ##
Ok, I have some time off coming up and will finally get this project updated to use the latest version of the plugins.  Stay tuned, and thanks to everyone who has had patience, and sorry to those that needed to go elsewhere :)


## 24 July 2010 Update ##
Well it is painfully obvious I haven't been back to this project for awhile now.  Still answering questions for people when you email through, and yes I am sure I will get back to this and 'refresh' the lot.

Bernie Lee, is a user who quite likes what this little program is doing and has created a straight forward user guide http://eeuserguide.wordpress.com/ which explains a lot about the program.  Great work Bernie, hopefully it assists others aswell.


## 11 January 2010 Update ##
Slow start to the year, will look at taking on board some of the suggestions emailed to do some more updates to this plugin.  It would appear from feedback that people would like this project extended in a variety of ways so as I find time will get this organised.

Thinking a better name (or at least a better style/logo) should be on the books aswell.


## 16 November 2009 Update ##
Forgot to add in when you create your includes you need to add one of the below classes to get the editing to fire.

class="e-ease" <- text area only

class="e-ease ee:wwig" <- full CKEditor

Also, had a request to enable a double click on the 'edit div' to trigger off the editing which can be easily done by adding...

```
jQuery(".e-ease").dblclick( function () { editNow(this.id); });
```

inside the **function bindEE()** .




## 12 November 2009 Update ##
1.5.1 - A little tweak completed to get around magic\_quotes if it exists on your server.

## 08 November 2009 Update ##

A very simple **jQuery CMS** that can be configured and set up in around 2 minutes.  Plugging in to your site is a breeze, and can be done at almost any time during the life cycle of development.

_**Installation file:** due to many requests I have now completed an installation script for this little plugin which is basic, but functional._

**Note:**  This is a very small CMS, with no database requirements.  Ideal for small sites, or where only a small amount of 'content management' is required.  If your site requires all content to be databased, there are many other CMS programs already in existence to choose from, so then maybe this is not the right solution. :)

## Demo Access NOW CLOSED ##


### Notes - Inclusions ###
**Modal windows are now handled by Eric Martins [SimpleModal](http://www.ericmmartin.com/projects/simplemodal/) a great plugin which should be considered for modal windows all the time.** WYSIWYG editor is now using the latest [CKEditor](http://ckeditor.com/), much faster than before and easily configurable (just look for the page _/**ee/cfk-edit.php** if you wish to configure past the basics I have done).  I have included a very basic 'Image Browse' list that reads data uploaded via the built in 'File Manager' of editEase._


## Found a problem or have a question ##
Please let me know if you find any problems (stating browser, OS etc...) with the nature of the problem, or send questions to
Stephen at noosalife at gmail dot com


## Whats Next ? ##
I know considering it too me nearly a year to find time for this update the 'next to do' items may take a little while.  That being said, I was thinking of a couple of new styles, a more in-depth 'ckeditor' file browser, some interaction with non .php pages and what ever else pops up through email requests.



## Basic Install Instructions: ##
**Start Installation**
  * Upload the _ee directory to your website and CHMOD 0777 or 0757 the
> > config.php file so it can be edited
  * Point browser to_ee/_eeInstall.php and fill in the form
  * CHMOD the inc files that can be edited
  * Delete_eeInstall.php file
**End Installation**

**Start Activation**
  * Reference editease.jquery.js (or the .min version) on each editable page
> > don't forget to reference jQuery of course
  * Add the activate script to the pages you wish to edit
  * thats it :)
**End Activation**

**Activation Script**
```
$(document).ready(function(){
	// load editEase login link and data into the page
	$("someDiv").editease(); <- can accept two variables
});

	// example with custom link name
	$("someDiv").editease('my admin');

	// example with overiding default path
	$("someDiv").editease('my admin','/demo/_ee'); 
```


> !important - The second variable with the overiding default path
> is useful when the folder _ee/ is not at the root of your website
> ie. its in a sub directory, on a local computer etc..._
