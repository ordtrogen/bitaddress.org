# bitaddress.org
JavaScript Client-Side Bitcoin Wallet Generator

Now Bitcoin addresses and their corresponding private key can be conveniently
generated in a web browser.

The bitaddress.org project provides an all-in-one HTML document with embedded
JavaScript/Css/Images. The JavaScript is readable not minified and contains no
XMLHttpRequest's (no AJAX). The benefit of this technique is you can load the
JavaScript locally and trust that the JavaScript did not change after being
loaded.

Here is a link to the BitcoinTalk.org forum topic discussing this project:
https://bitcointalk.org/index.php?topic=43496.0


Please send DONATIONS for this project to Bitcoin Address:
1NiNja1bUmhSoTXozBRBEtR8LeF9TGbZBN


END USER NOTES:

 1) For Bulk Wallet I recommended using Google Chrome, it's the fastest.

 2) Requires IE9+, Firefox, Chrome or sufficient JavaScript support.

 3) Mobile Safari only works with iPhone4 or newer devices.
    Older devices timeout while executing JavaScript.

 4) DO NOT use Opera Mini it renders JavaScript output server side, therefore
    they might record the private key you generated.

 5) BIP38 most likely will not work on mobile devices due to hardware limitations.

Notes for translators:
---------------------------------------
Here are some brief instructions on how to help out with a translation of the bitaddress.org page. If you want to improve or make corrections to an existing translation, just edit the existing language file in the folder src/culture and build the project using Grunt, which will be explained in a later section. There is, however, a chance that the existing language file is incomplete, so keep reading to find out how to find any missing strings that you may need to add.

If you're starting from scratch with a new language, make a copy of the file template.js in the src/culture folder and name the copy after the language it will contain. Let's say you will translate into Danish, so you name the file da.js. It will eventually contain all the translated strings for your language, but you can leave the file as is for now.

The complete set of strings that are used by the HTML page is listed in the file src/culture/localizables.json. It has this name because the process of transforming the user interface of an application from one language into another, is generally referred to as "localization". So, localizables.json contains the full set of strings that should be "localized". The reason it contains a JSON data structure is that this format can be read by many CAT tools (Computer Aided Translation). One such open source CAT tool which was used for the Swedish translation is called OmegaT and can be found

If you want to contribute to the project by creating a localized (translated) version of bitaddress.org, or improve on an existing localization, the file you need is in the folder src/culture. There, the files are named after the language they represent, es.js for Spanish, ru.js for Russian and so on.
Either create a new file for the language you intend to add (e.g da.js for Danish) or edit an existing file if you wish to make improvements or corrections.


Edit the following files:
Gruntfile.js:
Add a reference to your language file in the section below the comment "// cultures".




What Grunt does:

Download and install Grunt, ([link] http://gruntjs.com)

Look at the files in src/culture and select one whose language you're not too unfamiliar with. Let's say German, French or Spanish, if you're European. Make a copy of the file and give it the same name as the language code of your target language, e.g da.js or no.js if you're localizing into Danish or Norwegian. This file will be referred to as the "language file" in the following.

Open the file src/bitaddress-ui.html in a text editor. The file is encoded in UTF-8 format so make sure to use an appropriate editor. Add an entry for your language in the <div id="culturemenu"> near the beginning of the file's <body>. Then go to the section <script type="text/javascript"> with a number of commented-out language file names. Add your to the end, e.g //no.js

Go to Gruntfile.js and add your language file to the data structure "tokens". Make sure you get the syntax right. E.g if you add your entry to the end of the structure, you need to add a comma after the previous entry, to separate it from yours.

Run Grunt in the root directory where you checked out Bitaddress.org project.

(Run grunt on Windows... Use a Linux machine and set up a dropbox folder which you share with your Windows machine. Check out the git repo there and use Windows for editing the files. Install grunt-cli on the Linux box and use Putty from Windows to log on and run Grunt remotely on the Linux box.

If you want to see the English source of the strings your localizing, you can find them in bitaddress-ui.html where the id attribute of an html element will correspond to a string in the language file. E.g the text in <div id="bulka1" class="answer"> corresponds to the string "bulka1" in the array in your language file.
You can find some of the strings in ninja.translator.js
<span id="generatelabelmovemouse">








Notice of Copyrights and Licenses:
---------------------------------------
The bitaddress.org project, software and embedded resources are
copyright bitaddress.org.

The bitaddress.org name and logo are not part of the open source
license.

Portions of the all-in-one HTML document contain JavaScript codes that
are the copyrights of others. The individual copyrights are included
throughout the document along with their licenses. Included JavaScript
libraries are separated with HTML script tags.

Summary of JavaScript functions with a redistributable license:

JavaScript function	|	License
-------------------	|	--------------
Array.prototype.map	|	Public Domain
window.Crypto | BSD License
window.SecureRandom	| BSD License
window.EllipticCurve	|	BSD License
window.BigInteger |	BSD License
window.QRCode | MIT License
window.Bitcoin | MIT License

The bitaddress.org software is available under The MIT License (MIT)
Copyright (c) 2011-2013 bitaddress.org

Permission is hereby granted, free of charge, to any person obtaining
a copy of this software and associated documentation files (the
"Software"), to deal in the Software without restriction, including
without limitation the rights to use, copy, modify, merge, publish,
distribute, sublicense, and/or sell copies of the Software, and to
permit persons to whom the Software is furnished to do so, subject to
the following conditions:

The above copyright notice and this permission notice shall be
included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND,
EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF
MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND
NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE
LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION
OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION
WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.
