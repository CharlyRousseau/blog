---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: post
---
<html>
  <head>
    <div class='cadre'>
        <img id="image" src="{{site.baseurl}}/image/emergency.png">
    </div>
    <meta charset="utf-8">
    <img id="logo" src="{{site.baseurl}}/image/Among_Us_Logo.png" alt="" />
    <link href="{{site.baseurl}}/css/button.css" rel="stylesheet">
  </head>

  <body>

    <div id="alert"> <h1> ALERT </h1> </div>
    <div class="container">
        <a class="button"></a>




    <script>

      /*document.getElementById("showImage").onclick = function() {
      document.getElementById("theImage").style.visibility = "visible";*/
      let b1 = document.querySelector('a');
      let d1 = document.getElementById("image");
        b1.addEventListener('mousedown', function (e) {
        d1.classList.add('visible');
        playAudio();
        sendMessage();
        setTimeout("d1.classList.remove('visible');",2700);
      });
      function playAudio() {
          new Audio("{{site.baseurl}}/sounds/alert.ogg").play();
      }
      function sendMessage() {

        var request = new XMLHttpRequest();
        request.open("POST", "https://discordapp.com/api/webhooks/779079914615472160/BeMqvenvze_ri6dr4k64brSkdnm0nFerUujX-Ny3JrGFLlonz6w7oN90WkcgBomX8UXf");

        request.setRequestHeader('Content-type', 'application/json');

        var params = {
          username: "Among us ?",
          avatar_url: "",
          content: "",
          embeds: [
          {
            "author": {
            "name": "",
            "url": "",
            "icon_url": ""
          },
            "title": "ICI CA JOUE",
            "url": "",
            "description": "*@everyone* **Venez jouez !!!**.",
            "color": 15158332,
          }
          ]
        };

        request.send(JSON.stringify(params));
        //showImage();
      }
</script>
    </div>

 </body>

 </html>
