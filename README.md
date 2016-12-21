<script>
  (function(i,s,o,g,r,a,m){i['GoogleAnalyticsObject']=r;i[r]=i[r]||function(){
  (i[r].q=i[r].q||[]).push(arguments)},i[r].l=1*new Date();a=s.createElement(o),
  m=s.getElementsByTagName(o)[0];a.async=1;a.src=g;m.parentNode.insertBefore(a,m)
  })(window,document,'script','https://www.google-analytics.com/analytics.js','ga');

  ga('create', 'UA-89325718-1', 'auto');
  ga('send', 'pageview');

</script>
# mini-modalbox
Easy, Customized Modal Box - hardly 1.3 Byte minified version. Best Suitable for Small Purpose.

<p data-height="500" data-theme-id="dark" data-slug-hash="bBOejQ" data-default-tab="js,result" data-user="DesignerAshishOrg" data-embed-version="2" data-pen-title="Easy Customisable Mini Modal " class="codepen">See the Pen <a href="http://codepen.io/DesignerAshishOrg/pen/bBOejQ/">Easy Customisable Mini Modal </a> by Ashish Kumar (<a href="http://codepen.io/DesignerAshishOrg">@DesignerAshishOrg</a>) on <a href="http://codepen.io">CodePen</a>.</p>
<script async src="https://production-assets.codepen.io/assets/embed/ei.js"></script>


# Customization
Adjust below mentioned settings to your anchor tag as per requirement...

<pre><code>class="modal-button" </code>                 Modal-button must present on the anchor tag </pre>
<pre><code>data-height="50vh"</code>                    Define height of Modal Box </pre>
<pre><code>data-width="50vw"</code>                     Define width of Modal Box </pre>
<pre><code>data-title="Sample Popup"</code>             Define Heading of Modal Box </pre>
<pre><code>data-overlay-opacity="0.2"</code>            Define Overlay Opacity </pre>
<pre><code>data-overlay-color="blue"</code>             Define Overlay Color </pre>
<pre><code>data-animate-in="bounceInUp"</code>          Define the animation from list of animation in animate.css https://daneden.github.io/animate.css/  </pre>
<pre><code>data-animate-out="bounceOutDown"</code>      Define the animation from list of animation in animate.css https://daneden.github.io/animate.css/ </pre>
<pre><code>data-ajax=""</code>                          Ajax URL </pre>

# Javascript : Minified version 
<pre><code>jQuery(".modal-button").click(function(){var a={background:$(this).attr("data-overlay-color"),opacity:$(this).attr("data-overlay-opacity"),width:$(this).attr("data-width"),height:$(this).attr("data-height"),title:$(this).attr("data-title"),ajaxURL:$(this).attr("data-ajax"),animationIn:$(this).attr("data-animate-in"),animationOut:$(this).attr("data-animate-out")};$(".modal-container").removeClass(a.animationOut).addClass(a.animationIn),$(".modal-overlay").remove(),$("body").prepend('<div class="modal-overlay"></div>'),$(".modal-overlay").css("background",a.background),$(".modal-overlay").css("opacity",a.opacity),$(".modal-container").width(a.width),$(".modal-container").height(a.height),$(".modal-header").text(a.title),a.ajaxURL&&$.ajax({url:a.ajaxURL,data:{},beforeSend:function(){},statusCode:{404:function(){$(".modal-content").text("Page Not Found")}}}).done(function(a){$(".modal-content").html(a)}),$(".modal-container").fadeIn("fast",function(){});var t=$(window).width(),o=$(".modal-container").width();marLeft=(t-o)/2,$(".modal-container").css({"margin-left":marLeft}),$(".modal-header").append('<div class="modal-close">X</div>'),$(".modal-close").on("click",function(){$(this).parents(".modal-container").addClass(a.animationOut).removeClass(a.animationIn).fadeOut(),$(".modal-overlay").fadeOut()})});</code></pre>
