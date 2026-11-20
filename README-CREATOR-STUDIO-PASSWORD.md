# Creator Studio shared password (university demo)

This is a simple front-end password gate for Creator Studio. It is intended only as a lightweight demo barrier, not real security. The password is visible in the JavaScript source and can be bypassed by someone who inspects or modifies the browser code.


## Default demo password

`Ilovelyrics2026!`

## Change the password

Open `script.js` and find:

```js
const CREATOR_STUDIO_PASSWORD='Ilovelyrics2026!';
```

Replace the text between quotes with your own shared password. Keep it short enough to type comfortably, but do not reuse a personal or important password.

## Behavior

- Clicking Creator Studio opens the password modal.
- Correct password unlocks Creator Studio for the current visit.
- Navigating away from Creator Studio locks it again.
- The Lock Studio button locks and returns to Home.
- Incorrect passwords show an error message.
- This gate does not protect data or publishing from technical inspection; suitable only for a non-sensitive classroom demonstration.
