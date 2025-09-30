---
layout: page
title: Private Content
permalink: /private/
password: 821313
---

<div id="private-content" style="display:none;">
  <h2>  </h2>
  <p>   </p>
  <ul>
    <li><a href="{{ '/files/policy.pdf' | relative_url }}" download>ali</a></li>
  </ul>
</div>

<div id="password-form">
  <input type="password" id="password-input" placeholder="Enter password">
  <button onclick="checkPassword()">Submit</button>
  <p id="error-message" style="color:red; display:none;"></p>
</div>

<script>
function checkPassword() {
  const input = document.getElementById('password-input').value;
  const correctPassword = "{{ page.password }}";
  if (input === correctPassword) {
    document.getElementById('private-content').style.display = 'block';
    document.getElementById('password-form').style.display = 'none';
  } else {
    document.getElementById('error-message').style.display = 'block';
    document.getElementById('error-message').textContent = 'Incorrect password';
  }
}
</script>
