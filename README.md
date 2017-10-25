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

Notes to translators:
---------------------------------------
Here are some brief instructions on how to help out with a translation of the bitaddress.org page. If you want to improve or make corrections to an existing translation, just edit the corresponding language file in the folder src/culture and build the project using Grunt, which will be explained in a later section. There is, however, a chance that the existing language file is incomplete, so keep reading to find out how to find any missing strings that you might need to add.

If you're starting from scratch with a new language, make a copy of the file template.js in the src/culture folder and name the copy after the language it will contain. In these instructions, let's assume you'll translate into Danish, so you name the file da.js, since "da" is the language code for Danish. The file will eventually contain all translated strings for your language, but for now, just open it and change the part that says "LANGUAGE" to "da".

The complete set of strings that are used by the HTML page is contained in the file src/culture/localizables.json. It has this name because the process of transforming the user interface of an application from one language into another is generally referred to as "localization". So, localizables.json contains the full set of strings that should be "localized". If you're contributing to an existing translation, you may want to check if you need to copy (and translate) some strings from localizables.json that are not present in the existing language file. The reason it contains a JSON data structure is that this format can be read by many CAT (Computer Aided Translation) tools. One such open source CAT tool, which was used for the Swedish translation, is called OmegaT and can be found at http://omegat.org.

Leave localizables.json intact for future contributors and make a copy of it, preferably outside of the folder structure, which would make sense anyway if you use a tool like OmegaT as help. Translate the strings in the file, i.e. the string to the right of the colon on each line. When you're done, copy the entire contents of your translated file and paste it over the comment in your file "da.js".

If you're adding a new language, you'll need to edit the following files:

./Gruntfile.js :

Add a reference to your language file in the data structure below the comment "// cultures". Make sure you get the syntax right, it's easy to end up with a comma too much or too little.

./src/bitaddress-ui.html :

Add an entry for your language in the \<div id="culturemenu"\> element, corresponding to the existing ones.
Add a commented line referencing your language file in a <script> section near the end, where you can see the other language files listed.

The file ./bitaddress.org.html is not edited by hand but generated by a build process that uses ./src/bitaddress-ui.html as a template and includes the JavaScript files and produces ./bitaddress.org.html as output. The build process is done by a program called Grunt. Go to http://gruntjs.com and find the instructions for how to install and use it.

If all goes well you'll have a bitaddress.org.html file you can open in a browser and test. When everything works as expected, don't forget to make a pull request to contribute back your improvements to the original project.

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
