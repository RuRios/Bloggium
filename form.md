---
layout: page
title: Contact
permalink: /form/
---

<div class="container">
    <div class="col-1-2">
      <h1 style="font-weight: 900;">Functional HTML forms</h1>
      <h3 class="light">Just send your form to our URL and we'll forward it to your email. No PHP, Javascript or sign up required — <em>perfect for static sites!</em></h3>
    </div>
    <div class="col-1-2">
      <p>Example:</p>
      <p class="card code" style="font-size: small">
        &lt;form <span class="tooltip hint--top" data-hint="Use our URL as form's action">action="<span class="attr">//formspree.io/your@email.com</span>"</span><br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<span class="tooltip hint--top" data-hint="Forms must POST">method="<span class="attr">POST</span>"</span>&gt;<br>
        &nbsp;&nbsp;&nbsp;&nbsp;&lt;input type="<span class="attr">text</span>" name="<span class="attr">name</span>"&gt;<br>
        &nbsp;&nbsp;&nbsp;&nbsp;&lt;input type="<span class="attr">email</span>" <span class="tooltip hint--top" data-hint="Use advanced attributes">name="<span class="attr">_replyto</span>"</span>&gt;<br>
        &nbsp;&nbsp;&nbsp;&nbsp;<span class="tooltip hint--bottom" data-hint="When user submits, we'll email data to you">&lt;input type="<span class="attr">submit</span>" value="<span class="attr">Send</span>"&gt;</span><br>
        &lt;/form&gt;
      </p>
    </div>
</div>
