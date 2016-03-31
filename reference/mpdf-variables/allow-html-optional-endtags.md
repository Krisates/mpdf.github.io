---
layout: page
title: allow_html_optional_endtags
parent_title: mPDF Variables
permalink: /reference/mpdf-variables/allow-html-optional-endtags.html
---

<div id="bpmbook" class="bpmbook" style="direction:ltr;">
<div class="topic_user_field">
<div id="U0">
<p>(mPDF &gt;= 1.0)</p>
<h2>Description</h2>

<div class="alert alert-info" role="alert">boolean <b>allow_html_optional_endtags</b></div>
<p>When <span class="smallblock">TRUE</span>, mPDF will attempt to parse the input HTML allowing for omitted end-tags. Some end tags are optional in HTML 4 (see <a href="http://www.w3.org/TR/1998/REC-html40-19980424/index/elements.html">http://www.w3.org/TR/1998/REC-html40-19980424/index/elements.html</a>). These include (not exclusively): P, LI, DD, DT, TR, TD</p>

<div class="alert alert-info" role="alert"><b>Note:</b> If the HTML is incorrectly "formed" i.e. with illegal nesting of elements, this may do better or worse than the default.</div>
<h2>Values</h2>
<p class="manual_param_dt"><span class="parameter">allow_html_optional_endtags</span> = <i><span class="smallblock">TRUE</span></i>|<span class="smallblock">FALSE</span></p>
<p class="manual_param_dd"><b>Values</b>

<i><span class="smallblock">TRUE</span></i>: <span class="smallblock">DEFAULT</span> Parse the input HTML allowing for omitted end-tags

<span class="smallblock">FALSE</span>: Expect well formed (X)HTML with closing tags on all elements.</p>
<h2>Examples</h2>

{% highlight php %}
Example #1
{% endhighlight %}

{% highlight php %}
<?php

<?php

$mpdf=new mPDF();

$mpdf->allow_html_optional_endtags = true;

$mpdf->WriteHTML('<p>Hallo World');

$mpdf->WriteHTML('<p>Hallo World');

$mpdf->WriteHTML('<p>Hallo World');

$mpdf->Output();

?>
{% endhighlight %}

</div>
</div>
