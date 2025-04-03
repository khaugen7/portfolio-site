---
title: "Contact"
layout: "page"
---

## Let's get in touch

If you'd like to reach out, whether it's for opportunities, collaboration, or just to say hi,feel free to drop a message below.

<form name="contact" method="POST" netlify netlify-honeypot="bot-field" action="/thanks">
  <input type="hidden" name="form-name" value="contact" />
  <p style="display:none;">
    <label>Don’t fill this out if you’re human: <input name="bot-field" /></label>
  </p>
  <p>
    <label>Your Name:<br />
    <input type="text" name="name" required /></label>
  </p>
  <p>
    <label>Your Email:<br />
    <input type="email" name="email" required /></label>
  </p>
  <p>
    <label>Your Message:<br />
    <textarea name="message" rows="6" required></textarea></label>
  </p>
  <p>
    <button type="submit">Send Message</button>
  </p>
</form>
