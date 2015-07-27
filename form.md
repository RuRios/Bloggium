---
layout: page
title: Contact
permalink: /form/
---

<form>
  <input name="name" type='text' placeholder='Your name'>
  <input name="email" type='email' placeholder='Your email'>
  <input type="hidden" name="_subject" value="New submission!" >
  <textarea type="text" name="message2"></textarea>
  <button type='submit'>Apply</button>
</form>

<script>

var contactForm = contactSection.querySelector('form'),
    inputName = contactForm.querySelector('[name="name"]'),
    inputEmail = contactForm.querySelector('[name="email"]'),
    textAreaMessage = contactForm.querySelector('[name="message2"]'),
    sendButton = contactForm.querySelector('button');

    sendButton.addEventListener('click', function(event){
      event.preventDefault(); // prevent the form to do the post.

      sendButton.innerHTML = 'sending..';

      var xhr = new XMLHttpRequest();
      xhr.open('POST', '//formspree.io/rios.r@live.com', true);
      xhr.setRequestHeader("Accept", "application/json")
      xhr.setRequestHeader("Content-Type", "application/x-www-form-urlencoded")

      xhr.send(
        "name=" + inputName.value +
        "&email=" + inputEmail.value +
        "&subject=" + "XHR form" +
        "&message=" + textAreaMessage.value);

      xhr.onloadend = function (res) {
        if (res.target.status === 200){
          sendButton.innerHTML = 'Message sent!';
        }
        else {
          sendButton.innerHTML = 'Error!';
        }
      }
    });

</script>

<br><br>

 <form action="http://formspree.io/rios.r@live.com" method="POST">
    <input name="_replyto" type="email" placeholder="Your email">
    <textarea name="message" placeholder="Your message" rows="5"></textarea>
    <input name="_gotcha" style="display:none" type="text">
    <button type="submit">Send</button>
</form>
