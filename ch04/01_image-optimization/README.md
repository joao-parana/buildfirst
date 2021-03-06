# Image Optimization

![interlacing.gif][1]

In this example we'll losslessly compress images, while also applying a progressive interlacing transform to them. To this end, we use the [grunt-contrib-imagemin](https://github.com/gruntjs/grunt-contrib-imagemin) package.

To run the example, simply use `grunt build:release`.

```shell
grunt build:release
```

In the `debug` distribution, we set up a `copy` task similar to what can be seen in [**ch03e01** Distribution Config](https://github.com/bevacqua/buildfirst/tree/master/ch03/01_distribution-config "Distribution Config"), but for images instead. That's because we don't really need compression, nor interlacing, during `debug` builds.

```shell
grunt build:debug
```

That command will just copy the images, without any optimizations.

  [1]: http://i.imgur.com/oRX0u4V.gif "Interlacing is Fantastic, with Capital F."
