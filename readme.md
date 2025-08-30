# Animalese

Ever wanted to generate the talking sound from animal crossing? Well [this guy](https://github.com/Acedio/animalese.js/) solved that in 2014 (go star his repo not mine).
<br>Try it out online [here](http://acedio.github.io/animalese.js/)!

This library just makes his code work with modern javascript tooling (ES imports, type hints, etc). Try it in your browser console with `const { animalese, playSound } = await import("https://esm.sh/gh/jeff-hykin/animalese@1.0.1.0/animalese.js")`
 
```js
import { animalese, playSound } from "https://esm.sh/gh/jeff-hykin/animalese@1.0.1.0/animalese.js"

let pitch = 1 // range from 0 to 2
let shorten = false
const base64WavData = animalese("Hello", shorten, pitch).dataURI

// this next line only works in the browser (not deno or node js ... yet)
playSound("Hello World", {pitch: 1}).then(()=>console.log("audio finished"))
```
