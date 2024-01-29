# Animalese

Ever wanted to generate the talking sound from animal crossing? Well [this guy](https://github.com/Acedio/animalese.js/) solved that in 2014.
<br>Try it out online [here](http://acedio.github.io/animalese.js/)!

This library just makes his code work with modern javascript tooling.
 
```js
import { animalese, playSound } from "https://deno.land/x/animalese@1.0.0.0/animalese.js"

let pitch = 1 // range from 0 to 2
let shorten = false
const base64WavData = animalese("Hello", shorten, pitch).dataURI

// ONLY IN BROWSER
playSound("Hello World", {pitch: 1}).then(()=>console.log("audio finished"))
```