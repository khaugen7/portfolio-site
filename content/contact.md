---
title: "Contact"
layout: "page"
date: 2025-04-04
---

## Let's get in touch

If you'd like to reach out, whether it's for opportunities, collaboration, or just to say hi, feel free to drop a message below.

<form name="contact" method="POST" netlify netlify-honeypot="bot-field" action="/thanks/">
  <input type="hidden" name="form-name" value="contact" />
  <p style="display:none;">
    <label>Don’t fill this out if you’re human: <input name="bot-field" /></label>
  </p>
  <p>
    <label>Your Name:<br />
    <input type="text" name="name" required style="width: 60%; max-width: 600px; color: black;" />
  </p>
  <p>
    <label>Your Email:<br />
    <input type="email" name="email" required style="width: 60%; max-width: 600px; color: black;" />
  </p>
  <p>
    <label>Your Message:<br />
    <textarea name="message" rows="6" required style="width: 100%; max-width: 600px; color: black;"></textarea>
  </p>
  <p>
    <button type="submit" style="
  background-color: #1e40af;
  color: white;
  padding: 0.6rem 1.2rem;
  border: none;
  border-radius: 6px;
  font-weight: 600;
  cursor: pointer;
  transition: background-color 0.2s ease;
">
  Send Message
</button>

  </p>
</form>
