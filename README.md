# keyboard-diagnostics

A single static page (`index.html`) that logs what a phone's on-screen keyboard
does to a web page: focus and blur on the field and the window, page
visibility, key and `beforeinput`/`input` events, IME composition, form
submits (with their submitter), taps, and visual-viewport / VirtualKeyboard
geometry. Every line also records the element that has focus at that moment.

The composer mirrors a chat-style one: a `<form>` with a `<textarea>` and a
submit button, optionally inside a shadow root, optionally blurring the field
on send (touch devices only) or re-rendering itself after a send.

## Use

1. Open the page on the phone (GitHub Pages: <https://retog.github.io/keyboard-diagnostics/>).
2. Reproduce the problem, tap **Mark ★** right after it happens.
3. Tap **Copy log** and paste the log wherever it is needed.

The log survives a reload (kept in `localStorage`); **Clear** empties it.
