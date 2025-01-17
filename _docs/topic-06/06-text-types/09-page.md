---
title: Value
module: topic-06
permalink: /topic-06/text-value/
---

<div class="divider-heading"></div>

The `value` attribute "pre-fills" a text box. Unlike `placeholder`, when the user clicks in the text box, the "pre-filled" text is not replaced. Instead, the user can freely edit, remove, or keep it.


<div class="code-heading">
  <span class="html">HTML</span>
</div>

```html
<p>
  Birth Year:
  <input type="text" name="name" id="test-date" maxlength="4" size="4" value="19" />
</p>
```

<div class="row" style="margin-top: -30px;">
  <div class="col-lg-12">
    <div class="bs-component">
      <div class="panel panel-success">
        <div class="panel-heading">
          <h4 style="text-transform: uppercase; margin: inherit;">
            <i class="fa fa-check-circle" aria-hidden="true" style="margin-right: 10px"></i>
            Please Enter:
          </h4>
        </div>
          <div class="panel-body">
            <p style="font-size: large;">
              <span style="margin-right: 1em;">Birth Year:</span>
              <input type="text" name="name" id="test-date" maxlength="4" size="4" value="19" />
            </p>
            <p style="font-size: large;">
              <span style="margin-right: 2.6em;">Net ID:</span>
              <input type="text" name="name" id="test-text" placeholder="ab123456" />
            </p>
            <p style="font-size: large;">
              <span style="margin-right: 1.2em;">Password:</span>
              <input type="password" name="password" id="test-password" maxlength="15"/>
            </p>
            <p style="font-size: large;">
              <span style="margin-right: 1.26em;">Comments or Concerns:</span>
              <textarea name="comments" id="test-textarea" cols="20" rows="4" style="width:100%; border-color: #D8D8D8 !important; color: #777; font-size: medium">Enter up to 500 characters...</textarea>
            </p>
          </div>
      </div>
    </div>
  </div>
</div>


<span class="label label-info">NOTE:</span> This attribute can be used to fill "input" elements with data used "most of the time".
