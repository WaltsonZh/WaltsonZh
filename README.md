<head>
  <link href="./index.css" rel="stylesheet" type="text/css">
  <script src="./index.js"></script>
</head>
<div class="banner">
  <h1>Hi! I'm Waltson.</h1>
</div>

  <script>
    const banner = document.querySelectorAll('.banner')

    const randomColor = () => Math.floor(Math.random() * 256)

    const getContrast = (red, green, blue) => {
      // Calculate relative luminance
      const luminance = (0.299 * red + 0.587 * green + 0.114 * blue) / 255;

      // Use a simple threshold to determine if the color is light or dark
      return luminance > 0.5 ? 'black' : 'white';
    }

    console.log('hello')
    banner.forEach((b) => {
      b.addEventListener('click', () => {
        const red = randomColor()
        const green = randomColor()
        const blue = randomColor()
        b.style.background = `rgb(${red}, ${green}, ${blue})`
        b.style.color = getContrast(red, green, blue)
      })
    })
  </script>
