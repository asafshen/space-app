# Space App
An international space research that involve to discover the new space things

# Add Authentication
- Login to [Descope](https://sandbox.descope.com/login)
- Go [Projects page](https://sandbox.descope.com/settings/project). Copy your project ID
- Go to [Flows page](https://sandbox.descope.com/flows). Choose Flow to run and copy its ID
- Put the following code in index.html
```
<script src="./descope-wc.js"></script>
  <div class="login-container">
    <div class="login">
      <descope-wc 
        project-id="<project-id>"
        flow-id="<flow-id>"
        base-url="http://localhost:8000"
      >
      </descope-wc>
    </div>
  </div>
  <script>
    const descopeWcEle = document.getElementsByTagName('descope-wc')[0];
    descopeWcEle.addEventListener('success', () => {
      const el = document.querySelector('.login-container');
      el.parentElement.removeChild(el);
    });
  </script>
```
- Thats It!