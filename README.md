information on plotting can be found [here](https://nx10.github.io/httpgd/articles/a01_how-to-get-started.html)

plots can be displayed in the windows terminal as sixels, a special image format for terminals. To use do this install libsixel-bin

```sh
sudo apt update && sudo apt install lib-sixel
```

then you can use rush to plot

```sh
rush run 'print(mtcars)' | tee mtcars.csv
< mtcars.csv rush plot --x mpg --geom density --fill 'factor(cyl)' | img2sixel -w 600
```
