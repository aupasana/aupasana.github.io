---
layout: default
title: Test page for browser support
---

<div class="alert alert-info">
This page is designed to help determine browser support for the siddhanta font.
The user has to manually determine if the text renders correctly using the hints provided ...
this page does not perform any auto-detection or validation.
<button type="button" class="btn btn-secondary close" data-dismiss="alert">Dismiss</button>
</div>

<textarea rows="2" class="well form-control" id="UserAgent"></textarea>

<link href="{{ site.baseurl }}/css/vedicfonts-v10-modified.css" rel="stylesheet">
<link href="{{ site.baseurl }}/css/bootstrap-switch.min.css" rel="stylesheet">
<script src="{{ site.baseurl }}/js/bootstrap-switch.min.js"></script>

{::options parse_block_html="true" /}
<div class="browser-test">

{::options parse_block_html="true" /}
<div class="well">
## Anudatta and Svarita
  <div lang="sa">
  ॐ नमो भगवते॑ रुद्रा॒य
  </div>
* Is there a svarita above "te"?
* Is there an anudatta below "draa"?

<br/><input type="checkbox" class="browser-test-checkbox"/>
</div>

<div class="well">
## Dirgha svarita

  <div lang="sa">
  प्र॒जाप॑ते रोहि॒णीवे॑तु॒ पत्नी᳚।
  </div>
* Is there a svarita above "patnii"?
* Is it placed above the vowel (and not far off to the right)?

<br/><input type="checkbox" class="browser-test-checkbox"/>
</div>

<div class="well">
## Svarita above repha at beginning of samyuktakshara

  <div lang="sa">
  नि॒शीर्य॑ श॒ल्यानां॒ मुखा॑ शि॒वो नः॑ सु॒मना॑ भव ।
  </div>
* Is there a svarita above "rya"?
* Is the svarita placed above "rya" with no overlap?
* Is the svarita placed above "rya" (and not to the right)?

<br/><input type="checkbox" class="browser-test-checkbox"/>
</div>

<div class="well">
## Svarita above anusvara

  <div lang="sa">
  यामिषुं॑ गिरिशन्त॒ हस्ते॒ बिभ॒र्ष्यस्त॑वे।
  </div>
* Is there a svarita above "Shum"?
* Is the svarita placed above "Shum" with no overlap?
* Is the svarita placed above "Shum" (and not to the right)?

<br/><input type="checkbox" class="browser-test-checkbox"/>
</div>

<div class="well">
## Yajur veda anusvaras

  <div lang="sa">
  तेषा॑ꣳ सहस्रयोज॒नेऽव॒धन्वा॑नि तन्मसि॥  
  प॒शूꣴस्ताꣴश्च॑क्रे वाय॒व्यान्॑ ।
  </div>
* Does the taittiriya anusvara in "teShAm" render correctly?
* Do the taittiriya double anusvara in "pashuun taan"?
* Do they render in the siddhanta font (and not in some fallback font)?

<br/><input type="checkbox" class="browser-test-checkbox"/>
</div>

<div class="well">
## Yajur veda anusvaras with accents

  <div lang="sa">
  ये चे॒माꣳ रु॒द्रा अ॒भितो॑ दि॒क्षु श्रि॒ताः स॑हस्र॒शोऽवै॑षा॒ꣳ॒ हेड॑ ईमहे ॥  
  शि॒वां गि॑रित्र॒ तां कु॑रु॒ मा हिꣳ॑सीः॒ पुरु॑षं॒ जग॑त् ॥
  </div>
* Does the anudatta below "eShAm" render correctly?
* Does the udatta above "hiMsiiH" render correctly?
* Are the anusvaras rendered in the siddhanta font (and not in some fallback font)?

<br/><input type="checkbox" class="browser-test-checkbox"/>
</div>

<div class="well">
## Dirgha svarita above anusvara

  <div lang="sa">
  ग॒णानां᳚ त्वा ग॒णप॑तिꣳ हवामहे क॒विं क॑वी॒नामु॑प॒मश्र॑वस्तमम्।
  </div>
* Does the dirgha svarita above "gaNaanaaM" render correctly?
* Is it rendered above the anusvara (and not to the right)?
* Is it rendered with no overlap?

<br/><input type="checkbox" class="browser-test-checkbox"/>
</div>

<div class="well">
## Dirgha svarita above ra

  <div lang="sa">
  अहीꣳ॑श्च सर्वा᳚ञ्ज॒म्भय॒न्त्सर्वा᳚श्च यातुधा॒न्यः॑ ॥
  </div>
  * Does the dirgha svarita above "sarvan" render correctly?
  * Is it rendered above the repha (and not to the right)?
  * Is it rendered with no overlap?

  <br/><input type="checkbox" class="browser-test-checkbox"/>
</div>

<div class="well">
## Svarita precedes visarga

  <div lang="sa">
  ॐ नम॑ः शि॒वाय॑
  </div>
* Do both the svarita and visarga render correctly?
* Do they render without a box or dotted circle inbetween?

<br/><input type="checkbox" class="browser-test-checkbox"/>
</div>


<div class="well">
## Svarita follows visarga

  <div lang="sa">
  ॐ नमः॑ शि॒वाय॑
  </div>
  * Do both the svarita and visarga render correctly?
  * Do they render without a box or dotted circle inbetween?

  <br/><input type="checkbox" class="browser-test-checkbox"/>
</div>

<div class="well">
## Dirgha svarita precedes visarga

  <div lang="sa">
  अ॒स्मन्निव॑पन्तु॒ सेना᳚ः
  </div>
  * Do both the dirgha svarita and visarga render correctly?
  * Do they render without a box or dotted circle inbetween?

  <br/><input type="checkbox" class="browser-test-checkbox"/>
</div>

<div class="well">
## Dirgha svarita follows visarga

  <div lang="sa">
  अ॒स्मन्निव॑पन्तु॒ सेनाः᳚
  </div>
  * Do both the dirgha svarita and visarga render correctly?
  * Do they render without a box or dotted circle inbetween?

  <br/><input type="checkbox" class="browser-test-checkbox"/>
</div>

<div class="well">
## Dirgha svarita precedes anusvara

  <div lang="sa">
  ग॒णाना᳚ं त्वा ग॒णप॑तिꣳ हवामहे
  </div>
  * Do both the dirgha svarita and anusvara render correctly?
  * Do they render without a box or dotted circle inbetween?

  <br/><input type="checkbox" class="browser-test-checkbox"/>
</div>

<div class="well">
## Dirgha svarita follows anusvara

  <div lang="sa">
  ग॒णानां᳚ त्वा ग॒णप॑तिꣳ हवामहे
  </div>
  * Do both the dirgha svarita and anusvara render correctly?
  * Do they render without a box or dotted circle inbetween?

  <br/><input type="checkbox" class="browser-test-checkbox"/>
</div>

<div class="well">
## Svarita above consonant

  <div lang="sa">
  प॒शूꣳस्ताꣴश्च॑क्रे वाय॒व्यान्॑ ।
  </div>
* Does the svarita above "vayavyan" render correctly?
* Does it render above the consonant, and not to the right?
* Does it render without a box or dotted circle inbetween?

<br/><input type="checkbox" class="browser-test-checkbox"/>
</div>

<div class="well">
## Dirgha svarita above consonant

  <div lang="sa">
  यद्भू॒तं यच्च॒ भव्यम्᳚।
  </div>
  * Does the dirgha svarita above "bhavyam" render correctly?
  * Does it render above the consonant, and not to the right?
  * Does it render without a box or dotted circle inbetween?

  <br/><input type="checkbox" class="browser-test-checkbox"/>
</div>


<script type="text/javascript">
    $( document ).ready(function() {
      $.fn.bootstrapSwitch.defaults.size = 'small';
      $.fn.bootstrapSwitch.defaults.onText = 'Pass';
      $.fn.bootstrapSwitch.defaults.offText = 'Fail';
      $.fn.bootstrapSwitch.defaults.indeterminate = 'true';
      $.fn.bootstrapSwitch.defaults.onColor = 'success';
      $.fn.bootstrapSwitch.defaults.offColor = 'danger';
      $(".browser-test-checkbox").bootstrapSwitch();
      $('#UserAgent').val("UserAgent: ".concat(navigator.userAgent));
    });

</script>
