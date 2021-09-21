---
title: "Donation"
date: 2021-09-20T23:58:18-06:00
draft: false
---


<!-- content contains the main content of the page -->


<div style="height:230px;width:460px;margin-left:auto;margin-right:auto;border-width:0px;padding:0px;overflow:hidden;">

  <img id="image0" src="../images/donation_m007.jpg" alt="Empower Girls Through Math" style="width:230px;height:230px;border:0px;padding:0px;margin:0px;left:-230px;position:relative;display:block;z-index:0;">

  <img id="image1" src="../images/donation_m007.jpg" alt="Empower Girls Through Math" style="width:230px;height:230px;border:0px;padding:0px;margin:0px;left:0px;top:-230px;position:relative;display:block;z-index:0;">

  <img id="image2" src="../images/donation_m004.jpg" alt="Empower Girls Through Math" style="width:230px;height:230px;border:0px;padding:0px;margin:0px;left:230px;top:-460px;position:relative;display:block;z-index:0;">

</div>

<p style="font-family:arial,verdana,sans-serif; font-size:30px; text-align:center;">
  Empower Through Math
</p>

<script>
  var N = 23;
  var s1 = 7;
  var s2 = 4;
  $(document).ready(function(){
    setInterval("slidePix()", 30000);
  });

  function slidePix() {
    var sNew = s1;
    while ((sNew == s1) || (sNew == s2)) {
      sNew = Math.floor(Math.random()*(N+1));
    }
    $("img#image0").attr("src", makeName(sNew));
    $("img#image1").css("z-index", "1");
    $("img#image0").animate({left:'+=230px'}, 5000);
    $("img#image1").animate({left:'+=230px'}, 5000);
    $("img#image2").animate({left:'+=230px'}, 5000);
    $("img#image1").promise().done(function() {
      s2 = s1;
      s1 = sNew;
      $("img#image2").attr("src", makeName(s2))
      $("img#image2").animate({left:'230px'},1);
      $("img#image2").promise().done(function() {
        $("img#image1").css("z-index", "-1");
        $("img#image1").animate({left:'0px'},1);
        $("img#image1").attr("src", makeName(s1));
        $("img#image1").css("z-index","0");
        $("img#image0").css("z-index","-1");
        $("img#image0").animate({left:'-230px'},1);
        $("img#image0").css("z-index","0");
      });
    });
  }

  function makeName(imageNumber) {
    var prefix = "../images/donation_m";
    if ((imageNumber >= 0) && (imageNumber < 10)) {
      prefix = prefix.concat("00").concat(imageNumber.toString());
    } else if ((imageNumber > 9) && (imageNumber < 100)) {
      prefix = prefix.concat("0").concat(imageNumber.toString());
    } else if ((imageNumber > 99) && (imageNumber < 1000)) {
      prefix = prefix.concat(imageNumber.toString());
    } else {
      prefix = prefix.concat("001");
    }
    prefix = prefix.concat(".jpg");
    return prefix;
  }
</script>

<p>Support Quality Math Mentoring and Content Development. And remember,
   if it's good math for girls, it's good math for boys!</p>

<!--
<p>Donate using the Fleapay button below:</p>

<div style="height:75px;">

<script type="text/javascript" charset="utf-8" id="fp_product_embed_3ba304781a">
var fp_3ba304781a;
(function(b,c,a){if(!c.getElementById("fp-embed")){var d=c.getElementsByTagName("script")[0];a=c.createElement(a);a.type="text/javascript";a.async=!0;a.id="fp-embed";a.src="https://fleapay.s3.amazonaws.com/js/embed.min.js";d.parentNode.insertBefore(a,d)}fp=function(){try{fp_3ba304781a=new FleapayIFrame({fk:"2132593f698a74eb85434868b8c8e985",pk:"3ba304781a"}),fp_3ba304781a.prototype.create()}catch(e){}};b.addEventListener?b.addEventListener("load",fp,!1):b.attachEvent?b.attachEvent("onload",fp):b.onload=
fp})(window,document,"script");
</script>

</div>
-->
<p>Donate using the Paypal button below:</p>

<form action="https://www.paypal.com/cgi-bin/webscr" method="post" target="_top">
<input type="hidden" name="cmd" value="_s-xclick">
<input type="hidden" name="hosted_button_id" value="MG7L65RGMB6LA">
<input type="image" src="https://www.paypalobjects.com/en_US/i/btn/btn_donate_LG.gif" name="submit" alt="PayPal - The safer, easier way to pay online!" border="0">
<img alt="" src="https://www.paypalobjects.com/en_US/i/scr/pixel.gif" width="1" height="1" border="0">
</form>

<p>Or send a check made out to Girls' Angle and mail to Girls' Angle, PO Box 410038, Cambridge, MA 02141-0038.</p>

<p>If you wish to donate for a specific program within Girls' Angle (for example, if this is a
   Bulletin Sponsorship), please
   <a href="http://www.girlsangle.org/page/contact_us.html">email us</a> to let us know.</p>

<p>Girls' Angle is a nonprofit tax-exempt organization.  All donations are tax-deductible.</p>

<p>Thank you!</p>

<blockquote>A 2004 American Mathematical Society survey found that less than 6% of tenured faculty
  at 10 top US math departments were women. Facility with mathematics is important to an increasing
  number of professions including computer science, biostatistics, actuarial sciences, engineering, physics, and more.
</blockquote>

