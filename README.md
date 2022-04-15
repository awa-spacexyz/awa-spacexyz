![GithubBanner](https://user-images.githubusercontent.com/101623382/163571914-0177f0ee-a0a1-4ff3-9e5c-799faf64f3fe.jpg)

const express = require('express')
const app = express()

const PLACES = 7;

// no db - so global var to keep track of count
let counter = 0

function getCountImage(count) {
   ...
}

// get the image
app.get('/count.svg', (req, res) => {
  counter++;

  // This helps with GitHub's image cache 
  //   see more: https://rushter.com/counter.svg
  res.set({
  'content-type': 'image/svg+xml',
  'cache-control': 'max-age=0, no-cache, no-store, must-revalidate'
  })

  // Send the generated SVG as the result
  res.send(getCountImage(counter));
})

const listener = app.listen(process.env.PORT, () => {
  console.log('Your app is listening on port ' + listener.address().port)
})

<!--
**awa-spacexyz/awa-spacexyz** is a ✨ _special_ ✨ repository because its `README.md` (this file) appears on your GitHub profile.

Here are some ideas to get you started:

- 🔭 I’m currently working on ...
- 🌱 I’m currently learning ...
- 👯 I’m looking to collaborate on ...
- 🤔 I’m looking for help with ...
- 💬 Ask me about ...
- 📫 How to reach me: ...
- 😄 Pronouns: ...
- ⚡ Fun fact: ...
-->
