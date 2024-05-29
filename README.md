# forms
<form action="/my-handling-form-page" method="post">
  <ul>
    <li>
      <label for="name">Name:</label>
      <input type="text" id="name" name="user_name" />
    </li>
    <li>
      <label for="mail">Email:</label>
      <input type="email" id="mail" name="user_email" />
    </li>
    <li>
      <label for="msg">Message:</label>
      <textarea id="msg" name="user_message"></textarea>
    </li>
    <li class="button">
      <button type="submit">Send your message</button>
    </li>
  </ul>
</form>
form {
  margin: 0 auto;
  width: 400px;
  padding: 1em;
  border: 1px solid #ccc;
  border-radius: 1em;
}

div + div {
  margin-top: 1em;
}

label {
  display: inline-block;
  width: 90px;
  text-align: right;
}

input,
textarea {
  font-size: 1em;
  padding: 0.5em;
  border: 1px solid #ccc;
}
const form = document.querySelector('form');

form.addEventListener('submit', (e) => {
  e.preventDefault();
  const name = document.querySelector('#name').value;
  const email = document.querySelector('#mail').value;
  const message = document.querySelector('#msg').value;

  // Validate the form data here
  if (name === '' || email === '' || message === '') {
    alert('Please fill in all fields');
    return;
  }

  // Submit the form data
  form.submit();
});
