## Browser Object Model

* BOM Location
* BOM History
* BOM Navigator
* BOM Popup Alert
* BOM Timing
* BOM Cookies

* [JavaScript’s DOM Vs BOM](http://code-tricks.com/javascripts-dom-vs-bom/)


```js
<!DOCTYPE html>
<html>
    <head>
        <title>BOM</title>  
    </head>
<body>
    <!--Window Object-->

   <fieldset> <legend>Window-1</legend>
        <div>
            <input type="button" value="Open Google Window" onclick="openGoogleWindow()"><br /><br />

              <script>
                  function openGoogleWindow() {
                      //window.open("http://www.google.com");
                      window.open("http://www.google.com", "_blank", "toolbar=yes, location=yes, directories=no, status=no, menubar=yes, scrollbars=yes, resizable=no, copyhistory=yes, width=400, height=400");
                  }
            </script>

            <input type="button" value="Open new window" onclick="openWin()">
            <input type="button" value="Blur new window" onclick="blurWin()">
            <input type="button" value="Focus new window" onclick="focusWin()"><br /><br />

             <script>
                 var myWindow;
                 function openWin() {
                     myWindow = window.open("", "", "width=400, height=200");
                     myWindow.blur();
                 }

                 function blurWin() {
                     myWindow.blur();
                 }

                 function focusWin() {
                     myWindow.focus();
                 }
            </script>
        </div>

        <div>
            <input type="button" value="Open 'myWindow'" onclick="openMyWindow()" />
            <input type="button" value="Close 'myWindow'" onclick="closeMyWindow()" /><br /><br />
        </div>

        <script>
               var myOwnWindow;
               function openMyWindow() {
                   myOwnWindow = window.open("", "", "width=400, height=200");
               }

               function closeMyWindow() {
                   myOwnWindow.close();
               }

        </script>

    </fieldset>


    <fieldset> <legend>Window-2</legend>
        <div>
            <button onclick="openWin1()">Open myWindow</button>
            <button onclick="closeWin1()">Close myWindow</button>
            <button onclick="checkWin1()">Is myWindow open?</button>
            <input type="button" value="Move myWindow" onclick="moveWin()" />
            <input type="button" value="Move myWindow" onclick="moveWin1()" />
            <button onclick="Resize1()">Resize window</button>
            <button onclick="Resize2()">Resize window</button>
            <p id="IsmyWindowopen"></p><br /><br />

             <script>
                 var myWindow1, msg;
                 function openWin1() {
                     myWindow1 = window.open("", "", "width=400 ,height=200");
                     w.focus();
                 }

                 function closeWin1() {
                     if (myWindow1) {
                         myWindow1.close();
                     }
                 }

                 function checkWin1() {
                     msg = ""
                     if (!myWindow1) {
                         msg = "was never opened";
                     } else {
                         if (myWindow1.closed) {
                             msg = "is closed";
                         } else {
                             msg = "is open";
                         }

                     }
                     document.getElementById("IsmyWindowopen").innerHTML = "myWindow1 " + msg;
                 }

                 function moveWin() {
                     myWindow1.moveBy(250, 250)
                 }

                 function moveWin1() {
                     myWindow1.moveTo(300, 0);
                     myWindow1.focus();
                 }

                 function Resize1() {
                     myWindow1.resizeBy(50, 50);
                     myWindow1.focus();
                 }

                 function Resize2() {
                     w.resizeTo(500, 500);
                     w.focus();
                 }
            </script>

           
            <input type="button" value="Print this page" onclick="printPage()" /><br /><br />
            <script>
                function printPage() {
                    myWindow1.print();
                }
            </script>

            <input type="button" onclick="scrollWindow()" value="Scroll" /><br /><br />
            <script>
                //When the page is long
                function scrollWindow() {
                    window.scrollBy(0, 10);
                    // window.scrollTo(0, 100);
                }
            </script>
        </div>
    </fieldset>


      <!--Screen Object-->
    <fieldset> <legend>Screen Object</legend>

        <p id="screen_width"></p>
        <p id="screen_height"></p>
        <p id="screen_availWidth"></p>
        <p id="screen_availHeight"></p>
        <p id="screen_colorDepth"></p>
        <p id="screen_pixelDepth"></p>

        <script>
            document.getElementById("screen_width").innerHTML = "Screen width is " + screen.width;
            document.getElementById("screen_height").innerHTML = "Screen height is " + screen.height;
            document.getElementById("screen_availWidth").innerHTML = "Available screen width is " + screen.availWidth;
            document.getElementById("screen_availHeight").innerHTML = "Available screen height is " + screen.availHeight;
            document.getElementById("screen_colorDepth").innerHTML = "Screen color depth is " + screen.colorDepth;
            document.getElementById("screen_pixelDepth").innerHTML = "Screen pixel depth is " + screen.pixelDepth;
            document.getElementById("ow").innerHTML = window.outerWidth; 
            document.getElementById("oh").innerHTML = window.outerHeight; 
            document.getElementById("iw").innerHTML = window.innerHeight; 
            document.getElementById("ih").innerHTML = window.innerHeight; 
            document.getElementById("sw").innerHTML = window.screen.width; 
            document.getElementById("sh").innerHTML = window.screen.height; 
        </script>

    </fieldset>
    
     <!--Location Object-->
    <fieldset> <legend>Location Object</legend>
  
        <div>
            <p id="hostname"></p>
            <p id="href"></p>
            <p id="pathname"></p>
            <p id="protocol"></p>

            <script>
                document.getElementById("hostname").innerHTML = "Page hostname is: " + window.location.hostname;
                document.getElementById("href").innerHTML = "Page location is: " + window.location.href;
                document.getElementById("pathname").innerHTML = "Page path is: " + window.location.pathname;
                document.getElementById("protocol").innerHTML = "Page protocol is: " + window.location.protocol;
            </script>

            <input type="button" value="Load new document" onclick="window.location.assign('http://www.google.com')">
            <button onclick="window.location.replace('http://www.google.com')"> Replace document</button>
        </div>
    </fieldset>


    <!--History Object-->
    <fieldset> <legend>History Object</legend>
        <div>
            <button onclick="myFunction123()">History Length</button>
            <button onclick="goBack()">Go Back</button>
            <button onclick="goForward()">Go Forward</button>
            <button onclick="goBack()">Go 2 pages back</button>

            <p id="length"></p>

            <script>
                function myFunction123() {
                    document.getElementById("length").innerHTML = history.length;
                }

                function goBack() {
                    window.history.back()
                }

                function goForward() {
                    window.history.forward()
                }

                function goBack() {
                    window.history.go(-2)
                }
            </script>
        </div> 
    </fieldset>

  
     <!--Navigator Object-->
    <fieldset> <legend>Navigator Object</legend>
        <div>
            <p id="cookieEnabled"></p>
            <p id="appCodeName"></p>
            <p id="product"></p>
            <p id="appVersion"></p>
            <p id="userAgent"></p>
            <p id="platform"></p>
            <p id="language"></p>
            <p id="javaEnabled"></p>

            <script>
                    document.getElementById("cookieEnabled").innerHTML = "Cookies enabled is " + navigator.cookieEnabled;
                    document.getElementById("appCodeName").innerHTML = "Name is " + navigator.appName + "<br>Code name is " + navigator.appCodeName;
                    document.getElementById("product").innerHTML = "Browser engine is " + navigator.product;
                    document.getElementById("appVersion").innerHTML = navigator.appVersion;
                    document.getElementById("userAgent").innerHTML = navigator.userAgent;
                    document.getElementById("platform").innerHTML = navigator.platform;
                    document.getElementById("language").innerHTML = "Browser language is " + navigator.language;
                    document.getElementById("javaEnabled").innerHTML = "Java enabled is " + navigator.javaEnabled();
            </script>
        </div>
    </fieldset>

    <!--Popup Object-->
    <fieldset> <legend>Popup Object</legend>
         <div>

            <p id="confirm"></p>
            <p id="prompt"></p>

            <button onclick="alertsample()">Alert</button>
            <button onclick="confirmFunction()">Confirm</button>
            <button onclick="promptFunction()">Prompt</button>
        
            <script>
                function alertsample() {
                    alert("This is alert message box.");
                    alert("This is line 1\nThis is line 2?");
                }

                function confirmFunction() {
                    var x;
                    if (confirm("Do you want to continue!") == true) {
                        x = "OK - Clicked!";
                    } else {
                        x = "Cancel - Clicked!!";
                    }
                    document.getElementById("confirm").innerHTML = x;
                }

                function promptFunction() {
                    var person = prompt("Please enter your name", "Rams");

                    if (person != null) {
                        document.getElementById("prompt").innerHTML = "Hello " + person + "! How are you doing today?";
                    }
                }
            </script>
        </div>
    </fieldset>

   

    <!--Timing-->
    <fieldset> <legend>Timing Object</legend>
        <div>
            <button onclick="setTimeout(myFunction, 3000);">Greet after 3 seconds</button>
             <script>
                 function myFunction() {
                     alert('Hi Rams');
                 }
            </script>


            <button onclick="timedText()">Timed Text</button>
            <p id="timedText">Delayed Text update, display two, four, and six seconds have passed.</p>

            <script>
                function timedText() {
                    setTimeout(myTimeout11, 2000)
                    setTimeout(myTimeout21, 4000)
                    setTimeout(myTimeout31, 6000)
                }
                function myTimeout11() {
                    document.getElementById("timedText").innerHTML = "2 seconds";
                }
                function myTimeout21() {
                    document.getElementById("timedText").innerHTML = "4 seconds";
                }
                function myTimeout31() {
                    document.getElementById("timedText").innerHTML = "6 seconds";
                }
            </script>


          <br /><br />

            <button onClick="myTimer = setInterval(myCounter, 1000)">Start counter!</button>            
            <button onClick="clearInterval(myTimer)">Stop counter!</button>

             <script>
                 var c = 0;
                 function myCounter() {
                     document.getElementById("myCounter").innerHTML = ++c;
                 }
            </script>
            

             <br /><br />
            <button onclick="startTime()">Start Clock</button><p id="txt"></p>
            
             <script>
                 function startTime() {
                     var today = new Date();
                     var h = today.getHours();
                     var m = today.getMinutes();
                     var s = today.getSeconds();
                     m = checkTime(m);
                     s = checkTime(s);
                     document.getElementById('txt').innerHTML = h + ":" + m + ":" + s;
                     var t = setTimeout(startTime, 500);
                 }
                 function checkTime(i) {
                     if (i < 10) { i = "0" + i };  // add zero in front of numbers < 10
                     return i;
                 }
            </script>

            
            
            <p id="Clock">Clock</p>
            <button onclick="clearInterval(myTimer)">Stop Clock</button>

            <script>
                var myTimer = setInterval(myClock, 1000);
                function myClock() {
                    document.getElementById("Clock").innerHTML = new Date().toLocaleTimeString();
                }
            </script>
        </div>
    </fieldset>

     <!--Cookie-->
     <input type="button" value="Open new window" onclick="checkCookie()">
    <script>

        function setCookie(cname, cvalue, exdays) {
            var d = new Date();
            d.setTime(d.getTime() + (exdays * 24 * 60 * 60 * 1000));
            var expires = "expires=" + d.toGMTString();
            document.cookie = cname + "=" + cvalue + "; " + expires;
        }

        function getCookie(cname) {
            var name = cname + "=";
            var ca = document.cookie.split(';');
            for (var i = 0; i < ca.length; i++) {
                var c = ca[i];
                while (c.charAt(0) == ' ') {
                    c = c.substring(1);
                }
                if (c.indexOf(name) == 0) {
                    return c.substring(name.length, c.length);
                }
            }
            return "";
        }

        function checkCookie() {
            var user = getCookie("username");
            if (user != "") {
                alert("Welcome again " + user);
            } else {
                user = prompt("Please enter your name:", "");
                if (user != "" && user != null) {
                    setCookie("username", user, 30);
                }
            }
        }

</script>


</body>
</html>
```

![1](http://images.cnblogs.com/cnblogs_com/daibao9922/bom.gif)
![2](https://code.snipcademy.com/code/img/tutorials/javascript/bom/bom.svg)
![3](http://javascript.info/files/tutorial/browser/JSTop.png)
![6](https://www.visibone.com/products/ebk12-13_850.jpg)
![6](http://flylib.com/books/4/357/1/html/2/files/10fig03.gif)


