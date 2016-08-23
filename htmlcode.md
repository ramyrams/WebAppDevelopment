## ContentSectioning
```html
<!DOCTYPE html>
<html lang="en-us">
<head>
	<title>Awesome page title</title>
</head>
<body>

	 <!-- Content Sectioning -->
	<address>
		Written by <a href="mailto:webmaster@example.com">Jon Doe</a>.<br> 
		Visit us at:<br>
		Example.com<br>
		Box 564, Disneyland<br>
		USA
	</address>

	<article>
		<header>
			<h1>Most important heading here</h1>
			<h3>Less important heading here</h3>
			<p>Some additional information here</p>
			<hgroup>
				<h1>H1</h1> 
				<h2>H2</h2> 
				<h3>H3</h3> 
				<h4>H4</h4> 
				<h5>H5</h5> 
				<h6>H6</h6> 
			</hgroup>
		</header>
		<p>Lorem Ipsum dolor set amet....</p>
		<h1>WWF</h1>
		<section>
			<p>The World Wide Fund for Nature (WWF) is....</p>
		</section>
	</article>
	
    <header>
        <nav>
            <a href="/html/">HTML</a> |
            <a href="/css/">CSS</a> |
            <a href="/js/">JavaScript</a> 
        </nav>
    </header>

    <footer>
        <p>Posted by: Hege Refsnes</p>
        <p>Contact information: <a href="mailto:someone@example.com">someone@example.com</a>.</p>
    </footer>

</body>
</html>

```




## EditElements  
```html
<!DOCTYPE html>

<html lang="en-us">
<head>
	<title>Awesome page title</title>
</head>
<body>

	<!--Edit -->
    <!-- INS DEL-->  
    <p>My favorite color is <del>blue</del> <ins>red</ins>!</p>

</body>
</html>

```

## EmbeddedContent  
```html
<!DOCTYPE html>

<html lang="en-us">
<head>
	<title>Awesome page title</title>
</head>
<body>

    <!--Embedded Content -->
    <embed src="helloworld.swf" width="200" height="200 type="application/vnd.adobe.flash-movie" />

    <!--iframe -->
    <iframe src="demo_iframe_sandbox.htm"  name="iframe_a" width="200" height="200" sandbox></iframe>
    <iframe src="demo_iframe_sandbox_origin.htm" sandbox="allow-same-origin allow-scripts"></iframe>
    <iframe src="demo_iframe.htm"  srcdoc="<p>Hello world!</p>" seamless></iframe>

     <!--object & param -->
    <object data="horse.wav">
        <param name="autoplay" value="true">
    </object>
	
	<video controls>
		<source src="foo.webm" type="video/webm">
		I'm sorry; your browser doesn't support HTML5 video.
	</video>

</body>
</html>
```
## Forms  
```html
<!DOCTYPE html>

<html lang="en-us">
<head>
	<title>Awesome page title</title>
</head>
<body>


 <!-- --------------------->
    <!-- Form -->

     <!-- button. -->
    <button type="button">Click Me!</button>
    <button type="button" autofocus>Click Me!</button>
    <button type="button" disabled>Click Me!</button>
    <button type="button" onclick="window.location='http://www.littlewebhut.com'"> Go To Little Web Hut</button>

    <button type="reset" value="Reset">Reset</button>
    <button type="reset"><img src="yel.gif" alt="reset"><br>Reset</button>
    
    <button type="submit" name="subject" value="CSS" disabled="disabled">CSS</button>
    <button type="submit" formmethod="post" formaction="demo_post.asp" formenctype="text/plain" formtarget="_blank" formnovalidate >Submit using POST</button>
    




    <!-- A <fieldset> element located outside a form (but still a part of the form): -->
    <fieldset name="personalia" form="form1" disabled>
        <legend>Personalia:</legend>
        Name: <input type="text"><br>
        Email: <input type="text"><br>
    </fieldset>

     <!-- form & keygen -->
    <form action="demo_form.asp" accept-charset="ISO-8859-1" method="get" autocomplete="on" enctype="multipart/form-data" name="myForm"  target="_blank" novalidate>

        <keygen name="security" form="secureform" keytype="rsa" autofocus disabled>
    </form>

    <!-- label -->
    <label for="male" form="form1">Male</label>

     <!-- select, optgroup, option -->
    <select>
        <optgroup label="Swedish Cars">
            <option value="volvo">Volvo</option>
            <option value="saab">Saab</option>
        </optgroup>
        <optgroup label="German Cars">
            <option value="mercedes">Mercedes</option>
            <option value="audi">Audi</option>
        </optgroup>
    </select>


    <!-- datalist. -->

    <!--For the select element, the user is required to select one of the options you've given. 
        For the datalist element, it is suggested that the user select one of the options you've given, but he can actually enter anything he wants in the input. -->
    
    <input type=text list=browsers>
    <datalist id="browsers">
        <option value="Internet Explorer">
        <option value="Firefox">
        <option value="Google Chrome">
    </datalist>



    <!-- meter -->
    <meter form="form1" name="x1" min="0" low="40" high="90" max="100" value="95" optimum="0.5"></meter>

     <!-- progress -->
    <progress value="22" max="100"></progress>

    <!-- output -->
    <form oninput="x.value=parseInt(a.value)+parseInt(b.value)">0
        <input type="range" id="a" value="50">100 + <input type="number" id="b" value="50"> = <output name="x" for="a b"></output>
    </form>

    <!-- textarea -->
    <textarea rows="4" cols="50">At w3schools.com you will learn how to make a website. </textarea> 

    <!-- input -->
    <input type="text" id="someInput" name="pin" maxlength="4" size="4" placeholder="First name" required autofocus pattern="[A-Za-z]{3}" title="Three letter country code">
    <input type="text" name="country" value="Norway" readonly disabled>

    <input type="file" name="pic" accept="image/*" multiple>

    <input type="image" src="submit.gif" alt="Submit" width="48" height="48">

    
    <input type="checkbox" name="vehicle" value="Bike"> I have a bike<br>
    <input type="checkbox" name="vehicle" value="Car" checked> I have a car<br>

    <input type="radio" name="gender" value="male"> Male<br>
    <input type="radio" name="gender" value="female"> Female

    
    <input type="number" name="quantity" min="1" max="50" step="3">
    
    <input type="password" name="pw" pattern=".{6,}" title="Six or more characters">
    <input type="password" name="pw" pattern="(?=.*\d)(?=.*[a-z])(?=.*[A-Z]).{8,}" title="Must contain at least one number and one uppercase and lowercase letter, and at least 8 or more characters">

    <input type="search" name="googlesearch" pattern="[^'\x22]+" title="Invalid input">
    
	<input type="tel" name="usrtel">
    <input type="url" name="website" pattern="https?://.+" title="Include http://">
    <input type="email" name="email" autocomplete="off" pattern="[a-z0-9._%+-]+@[a-z0-9.-]+\.[a-z]{2,3}$">
 
    <input type="reset">
    
    <input type="button" value="Click me" onclick="msg()">

    <input type="submit" formaction="demo_admin.asp" formmethod="post" value="Submit as admin"  formnovalidate="formnovalidate" formenctype="multipart/form-data" formtarget="_blank">
   
    <input type="date" name="bday" max="1979-12-31" min="2000-01-02">
    <input type="time" name="usr_time">
    <input type="datetime" name="bdaytime">
    <input type="month" name="bdaymonth">
    <input type="datetime-local" name="bdaytime">
    <input type="week" name="week_year">

    <input type="hidden" name="country" value="Norway">
    
    <input type="color" name="favcolor">

    <input type="range" name="points" min="0" max="10">

    <input list="browsers">
	
	
    

</body>
</html>

```


## InlineText  
```html
<!DOCTYPE html>

<html lang="en-us">
<head>
	<title>Awesome page title</title>
</head>
<body>

<!-- Inline text semantics
Use the HTML inline text semantic to define the meaning, structure or style of a word, line or portion of text. -->


<!-- A Tag -->
    <!--
    The URL of the link.
        An absolute URL - points to another web site (like href="http://www.example.com/default.htm")
        A relative URL - points to a file within a web site (like href="default.htm")
        Link to an element with a specified id within the page (like href="#top")
        Other protocols (like https://, ftp://, mailto:, file:, etc..)
        A script (like href="javascript:alert('Hello');")
        -->
    <a href="http://www.littlewebhut.com">Visit Little Web Hut</a>
    <a href="http://www.littlewebhut.com">   <img src="http://www.littlewebhut.com/images/little_web_hut.gif"    alt="Little Web Hut"></a>
    <a href="#example4">Jump to Ten</a>
    <a href="example_a1.html">Example</a>
    <a href="examples/example_a2.html">Example</a>
    <a href="../example_a3.html">Example</a>
    <a href="example_a4.html#example4">Jump to Ten</a>
    <a href="http://www.littlewebhut.com" target="_top" >Visit Little Web Hut</a>
    <a href="/images/myw3schoolsimage.jpg" download>
    <a href="/images/myw3schoolsimage.jpg" download="w3logo">
    <a href="mailto:someone@example.com?Subject=Hello%20again">Send mail!</a>
    <a href="mailto:someone@example.com?cc=someoneelse@example.com&bcc=andsomeoneelse@example.com&subject=Summer%20Party&body=You%20are%20invited%20to%20a%20big%20summer%20party!">Send mail!</a>
    <a href="javascript:alert('Hello World!');">Execute JavaScript</a>
    <a href="http://www.w3schools.com" hreflang="en">W3Schools</a>
    <a href="att_a_media.asp?output=print" media="print and (resolution:300dpi)">Open media attribute page for print.</a>
    <a href="http://www.w3schools.com" type="text/html">W3Schools</a>
    <a href="cakes.html" accesskey="c">lovely range of cakes [access key = c]</a>
    <a href="cakes-ja.html" charset="euc-jp">lovely range of Japanese cakes (note: this link will take you to a page in Japanese language)</a>
    <a href="http://www.djformat.com/" rel="friend">Matt</a>
    <a href="cakes.html" rel="product-line" rev="menu-index">lovely range of cakes</a>
    <a href="theweasel.html" shape="poly" coords="136,238,137,301,3,306,3,242">Thursday's mustache - 'The Weasel'</a>
    <a href="cakes.html" tabindex="3">lovely      range of cakes</a> 
	
	<a rel="nofollow noreferrer" href="http://amzn.to/1JunkLD">Buy me a Macbook Pro</a>

	
	<!-- http://sixrevisions.com/html/link-types-hyperlinks/ -->
	<!--  The content in PDF format -->
	<a rel="alternate" type="application/pdf" href="this-page.pdf">PDF version</a>

	<!-- Download the web page -->
	<a rel="alternate" type="application/zip" href="this-page.zip" download>Download this web page</a>

	<!-- Read the content in Spanish -->
	<a rel="alternate" hreflang="es" href="spanish-version.html">Read this page in Spanish</a>

	<!-- Read the content in Tagalog -->
	<a rel="alternate" hreflang="tl" href="tagalog-version.html">Read this page in Tagalog</a>

	<a rel="author" href="my-author-bio.html">About Me</a>
	<a rel="author" href="someone-else.html">About Someone Else</a>

	
	 <a rel="bookmark" href="blog-post.html">Read this</a>
	 
	 <a rel="help" href="comments.html">Commenting Help</a>
	 
	 <!-- This photo is in the public domain -->
	<img src="free-photo.jpg" />
	<p>License: <a rel="license" href="https://creativecommons.org/publicdomain/zero/1.0/">CC0</a></p>
  
	 
	 <a rel="nofollow" href="http://paid.example.co">A paid link</a>
	 
	 <a rel="noreferrer" href="http://faceup.com">Don't track this link</a>
	 
	 <a rel="prefetch" href="large.jpg" title="Go to a larger version of the photo."><img src="small.jpg" alt="Small preview of the photo." /></a>
	 
	 <a rel="search" href="#search">Search this page</a>
	 
	 <a rel="tag" href="http://sixrevisions.com/category/html">HTML</a> category.</p>
	 
	 <a rel="prev" href="1st.html">
	 
	 <a rel="next" href="3rd.html">
	 
	<a href="http://www.w3schools.com/html5" accesskey="h">HTML5</a><br>
	<a href="http://www.w3schools.com/css3" accesskey="c">CSS3</a>


	<a href="http://www.w3schools.com/" tabindex="2">W3Schools</a>
	<a href="http://www.google.com/" tabindex="1">Google</a>
	<a href="http://www.microsoft.com/" tabindex="3">Microsoft</a>

		
	<!-- abbr Tag 
    an abbreviation is a shortened form of a word (e.g. abbreviation => abbr, ex: lb., amt., mgmt.   -->
    The <abbr title="World Health Organization">WHO</abbr> was founded in 1948.

    <!-- b -->
    <p>The MrBigStuff logo was a mixture of normal and bold characters: "Mr <b>Big</b> Stuff"</p>

    <!--- bdo stands for Bi-Directional Override. -->
    <bdo dir="ltr">Text written right to left.</bdo>
    <bdo dir="rtl">Text written left to right.</bdo>

    <!-- Bi-directional Isolation. -->
    <ul>
        <li>User <bdi>hrefs</bdi>: 60 points</li>
        <li>User <bdi>إيان</bdi>: 90 points</li>
    </ul>

    <!-- br. -->
    This text contains<br>a line break.

    <!-- cite. -->
    <p><cite>The Scream</cite> by Edward Munch. Painted in 1893.</p>

     <!-- code. -->
     <code>A piece of computer code</code>

	<!-- data -->
	<p>New Products</p>
	<ul>
		 <li><data value="3967381398">Mini Ketchup</data></li>
		 <li><data value="3967381399">Jumbo Ketchup</data></li>
		 <li><data value="3967381400">Mega Jumbo Ketchup</data></li>
	</ul>

    <!-- dfn -->
    <p><dfn>HTML</dfn> is the standard markup language for creating web pages.</p>
   
    <!-- em -->
    <em>Emphasized text</em>

    <!-- i-->
    <p>He named his car <i>The lightning</i>, because it was very fast.</p>

    <!-- kbd -->
    <p>To get a list of directories, type <kbd>dir</kbd> in the command line and press Enter.</p>
  
    <!-- kbd -->
    <p>Do not forget to buy <mark>milk</mark> today.</p>

    <!-- kbd -->
    <p>WWF's goal is to:  <q>Build a future where people live in harmony with nature.</q> We hope they succeed.</p>

	<!-- ruby, rt, rp -->
	<ruby>
	   <rb>旧</rb>
	   <rb>金</rb>
	   <rb>山</rb>
	   <rt>jiù</rt>
	   <rt>jīn</rt>
	   <rt>shān</rt>
	   <rtc>San Francisco</rtc>
	</ruby>

    <!-- s -->
    <p><s>My car is blue.</s></p>

    <!-- samp -->  
    <samp>Sample output from a computer program</samp>

    <!-- small -->  
    <p><small>Copyright 1999-2050 by Refsnes Data</small></p>

    <!-- <span>-->
    <p>My mother has <span>blue</span> eyes.</p>

    <!-- strong -->  
    <strong>Strong text</strong>

    <!-- sup -->  
    <p>This text contains <sup>superscript</sup> text.</p>

    <!-- sub -->  
    <p>This text contains <sub>subscript</sub> text.</p>

   
    
    <!-- TIME --> 
    <p>I have a date on <time datetime="2008-02-14 20:00">Valentines day</time>.</p>

    <!-- u --> 
    <p>This is a <u>parragraph</u>.</p>
    
    <!-- var --> 
    <var>Variable</var>

    <!-- Word Break Opportunity -->
    <p>To learn AJAX, you must be familiar with the XML<wbr>Http<wbr>Request Object.</p>

	

<body>
</html>

```

## InteractiveElements  
```html
<!DOCTYPE html>

<html lang="en-us">
<head>
	<title>Awesome page title</title>
</head>
<body>

    <!-- Interactive elements -->

    <!-- details & summary -->
    <details>
          <summary>Copyright 1999-2014.</summary>
          <p> - by Refsnes Data. All Rights Reserved.</p>
          <p>All content and graphics on this web site are the property of the company Refsnes Data.</p>
    </details>

    <!-- dialog -->
    <dialog open>
		<p>Greetings, one and all!</p>
	</dialog>
	

     <!-- menu & menuitem -->
    <menu type="context" id="mymenu">
        <menuitem label="Refresh" onclick="window.location.reload();" icon="ico_reload.png" checked command="submitbutton" default> </menuitem>
        <menuitem type="radio" label="Left" radiogroup="alignment" onclick="setAlign('left')">Left</menuitem>
        <menuitem type="command" label="Save" onclick="save()">Save</menuitem>

        <menu label="Share on...">
            <menuitem label="Twitter" icon="ico_twitter.png" onclick="window.open('//twitter.com/intent/tweet?text='+window.location.href);" disabled> </menuitem>
            <menuitem label="Facebook" icon="ico_facebook.png" onclick="window.open('//facebook.com/sharer/sharer.php?u='+window.location.href);"></menuitem>
        </menu>

        <menuitem label="Email This Page" onclick="window.location='mailto:?body='+window.location.href;"></menuitem>
    </menu>
	

</body>
</html>


```

## Meta_Elements  
```html
<!DOCTYPE html>

<html lang="en-us">
<head>

	<title>Awesome page title</title>

    <!-- BASE Tag -->
    <base href="http://www.rams1.com" target="right"/>
    
    <!-- LINK Tag -->
    <link rel="stylesheet" href="basic.css"/>
    <link rel="stylesheet" type="text/css" href="/stylesheets/basic.css"/>
    <link rel="stylesheet" type="text/css" href="../basic.css"/>
    <link rel="stylesheet" href="basic.css" media="screen, projection"/>
    <link rel="stylesheet" href="print.css" media="print"/>
    <link rel="stylesheet" type="text/css" href="http://www.somedomainname.com/stylesheets/basic.css"/>
    <link rel="stylesheet" type="text/css" href="data:text/css,body%20{%20background%3A%20green%3B%20}"/>
    <link rel="stylesheet" type="text/css" href="data:text/css;base64,Ym9keSB7IGJhY2tncm91bmQ6IGdyZWVuOyB9"/>

	<link href="default.css" rel="stylesheet" title="Default Style">
	<link href="fancy.css" rel="alternate stylesheet" title="Fancy">
	<link href="basic.css" rel="alternate stylesheet" title="Basic">

    <link rel="alternate stylesheet" title="Higher Contrast" href="contrast.css" type="text/css" media="screen"/>
    <link rel="alternate stylesheet" title="Gratuitous CSS" href="hot.css" type="text/css" media="screen"/>
    
    <link rel="parent"      href="okinawa.html" charset="euc-jp"/>
    <link rel="subsection"  href="categories.html" rev="parent" target="subframe" />

    <link rel="alternate" type="application/rss+xml" href="/rss.xml" title="RSS 2.0">
    <link rel="alternate" type="application/atom+xml" href="/atom.xml" title="Atom 1.0">

    <link rel="shortcut icon" href="/favicon.ico"/>

    
    <!-- META Tag -->
	<meta charset="utf-8">
	<meta property="og:site_name" content="Gizmo's Freeware">
	
    <meta name="application-name" content="My App" charset="UTF-8">
    <meta name="department" content="Technology">
    <meta name="author" content="John Smith">
    <meta name="appearance" content="fluffy">
    <meta name="categories" content="work, projects, current"/>
	
	<meta name="Generator" content="Drupal 7 (http://drupal.org)">
	<meta name="viewport" content="width=device-width, initial-scale=1">
	<meta name="MobileOptimized" content="width">
	<meta name="HandheldFriendly" content="true">
	<meta name="apple-mobile-web-app-capable" content="yes">

	<link rel="shortlink" href="/node/1209">
	
    <!-- comma-separated list of keywords that apply to the page -->
    <meta name="keywords" content="reference, SitePoint, HTML, XHTML, standards">
    <meta name="description" content="A brief summary/description of the content on the page, which may appear in search engine results">

    <!-- sets character encoding -->
    <meta http-equiv="Content-Type" content="text/html; charset=UTF-8">
    <meta http-equiv="default-style" content="the document's preferred stylesheet">

    <!-- refreshes the page content every five seconds -->
    <meta http-equiv="Refresh" content="5">

    <!-- instructs search engines not to index this page, but to follow links from the page -->
    <meta name="robots" content="noindex,follow">

    <meta name="DC.date" content="2003-06-08" scheme="DCTERMS.W3CDTF" />

    <!-- script Tag -->  
    <script type="text/javascript" src="/scripts/common.js" charset="ISO-8859-15" language="JavaScript1.2" xml:space="preserve" defer="defer"></script>
    
    <!-- style Tag --> 
    <style type="text/css" media="screen, projection" xml:space="preserve"></style> 

    <style>
        .myDiv {
           color:yellow;
        }
    </style>
  
</head>
<body>
<p>Metadata elements</p>

</body>
</html>

```

## Multimedia  
```html
<!DOCTYPE html>

<html lang="en-us">
<head>
	<title>Awesome page title</title>
</head>
<body>

    <!--Image & multimedia-->
	<img src="mdn-logo-sm.png" alt="MDN">
	<a href="https://developer.mozilla.org/"><img src="mdn-logo-sm.png" alt="MDN"></a>
	<img src="mdn-logo-sm.png"  alt="MDN" srcset="mdn-logo-HD.png 2x">
	<img src="clock-demo-thumb-200.png" alt="Clock"  srcset="clock-demo-thumb-200.png 200w, clock-demo-thumb-400.png 400w" sizes="(min-width: 600px) 200px, 50vw">
	
	
   <!--video,  track -->
    <video width="320" height="240" preload controls>
        <source src="forrest_gump.mp4" type="video/mp4">
        <source src="forrest_gump.ogg" type="video/ogg">
        <track src="subtitles_en.vtt" kind="subtitles" srclang="en" label="English">
        <track src="subtitles_no.vtt" kind="subtitles" srclang="no" label="Norwegian">
    </video>

    <!--audio -->
    <audio autoplay="autoplay" controls="controls">
         <source src="movie.ogg" type="video/ogg" media="screen and (min-width:320px)">
        <source src="file.mp3" /> 
        <a>Download this file.</a>
    </audio>

    <!-- img, map,  area-->
    <img src="planets.gif" width="145" height="126" alt="Planets" usemap="#planetmap">
    <map name="planetmap">
      <area shape="rect" coords="0,0,82,126" href="sun.htm" alt="Sun">
      <area shape="circle" coords="90,58,3" href="mercur.htm" alt="Mercury">
      <area shape="circle" coords="124,58,8" href="venus.htm" alt="Venus">
    </map>

</body>
</html>

```

## Scripting  
```html
<!DOCTYPE html>

<html lang="en-us">
<head>
	<title>Awesome page title</title>
</head>
<body>

    <!--scripting -->
    
    <canvas id="Canvas1" width="200" height="200" style="border:1px solid"></canvas>

	<noscript>
		<!-- anchor linking to external file -->
		<a href="http://www.mozilla.com/">External Link</a>
	</noscript>

    <script src="javascript.js"></script>

</body>
</html>

```

## TableContent  
```html
<!DOCTYPE html>

<html lang="en-us">
<head>
	<title>Awesome page title</title>
</head>
<body>

	<!-- Table Content -->

    <!--table, caption, colgroup, col, thead, tbody, tfoot, th, tr, td-->
   <table>
        <caption>Sales Summary</caption>

        <!--    The <colgroup> tag specifies a group of one or more columns in a table for formatting.
            The <colgroup> tag is useful for applying styles to entire columns, instead of repeating the styles for each cell, for each row.-->
         <!--Note: The <colgroup> tag must be a child of a <table> element, after any <caption> elements and before any <thead>, <tbody>, <tfoot>, and <tr> elements.-->
        <colgroup>
            <col span="2" style="background-color:red">
            <col style="background-color:yellow">
        </colgroup>

          <tfoot>
              <tr>
                 <td>City</td>
                 <td>Sum</td>
                 <td>$180</td>
              </tr>
         </tfoot>

        <thead>
            <tr>
                <th>City</th>
                <th>Month</th>
                <th>Savings</th>
            </tr>
        </thead>


        <tbody>
            <tr>
                <td>Fremont</td>
                <td>January</td>
                <td>$100</td>
             </tr>
            <tr>
                <td>Fremont</td>
                <td>Feb</td>
                <td>$80</td>
            </tr>
        </tbody>    
  
    </table>

</body>
</html>


```

## TextContent  
```html
<!DOCTYPE html>
<html lang="en-us">
<head>
	<title>Awesome page title</title>
</head>
<body>

	<!-- Text content -->
	<!-- Use HTML text content elements to organize blocks or sections of content placed between the opening <body> and closing </body> tags. 
	Important for accessibility and SEO, these elements identify the purpose or structure of that content.  -->

	<!-- List elements -->
    <!-- DL, DT, DD -->
    <dl>
        <dt>Spam</dt>
        <dd>unsolicited email sent in the hope of increasing sales of some product, or simply for the purposes of annoying people
            <dl>
                <dt>Spammer</dt>
                <dd>someone who sends out spam email and therefore deserves to develop a nasty incurable disease of some kind</dd>
    
                <dt>Spam Filter</dt>
                <dd>a tool used in email to 'filter out' likely spam messages,usually placing them in a dedicated junk messages folderor similar</dd>
            </dl>
        </dd>
    </dl>

     <!-- DIV -->
    <div >
        <h3>This is a heading</h3>
        <p>This is a paragraph inside DIV.</p>
    </div>
    
	<!--  HTML5 Custom Data- Attribute-->
	<div id="div1" class="style" data-time="3" data-order="1"></div>
	<div id="div2" class="style" data-time="5" data-order="3"></div>
	<div id="div3" class="style" data-time="2" data-order="2"></div>
	<div dropzone="copy"></div>
		
		
     <!-- P -->
    <p> This is paragraph</p>
	<p dir="rtl">Write this text right-to-left!</p>
	<p draggable="true">This is a draggable paragraph.</p>
	<p hidden>This paragraph should be hidden.</p>
	<p lang="fr">Ceci est un paragraphe.</p>
	<p contenteditable="true" spellcheck="true">This is a paragraph.</p>
	<p style="color:green">This is a paragraph.</p>
	<p translate="no">Don't translate this!</p>
	<p contenteditable="true">This is an editable paragraph.</p>

		
    <!-- HR -->
    <hr />

    <!-- UL, OL, LI-->
    <ul  contenteditable="true">
        <li>Eggs</li>
        <li>Cheese</li>
        <li>Milk</li>
    </ul>

    <ol>
        <li>Eggs</li>
        <li>Cheese</li>
        <li>Milk</li>
    </ol>

    <!-- FIGURE, FIGCAPTION -->
    <figure>
        <img src="img_pulpit.jpg" alt="The Pulpit Rock" width="304" height="228">
        <figcaption>Fig1. - A view of the pulpit rock in Norway.</figcaption>
    </figure>

    <!--PRE -->
    <pre>
                Text in a pre element
                is displayed in a fixed-width
                font, and it preserves
                both      spaces and
                line breaks
	
    </pre>
	
	 <pre>
		 o           .'`/
			 '      /  (
		   O    .-'` ` `'-._      .')
			  _/ (o)        '.  .' /
			  )       )))     ><  <
			  `\  |_\      _.'  '. \
				'-._  _ .-'       '.)
			jgs     `\__\
	</pre>
 
 
 
	
	<main>
		<h1>Apples</h1>
		<p>The apple is the pomaceous fruit of the apple tree.</p>
	</main>

</body>
</html>

```
