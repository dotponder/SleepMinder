# SleepMinder
一个睡眠监测Android程序

主要源码由[@Sopamo]([Sopamo/sleepminder: A sleep monitoring application for Android. Includes a framework to create custom sleep monitoring apps. This application is a demonstration of the library's features. (github.com)](https://github.com/Sopamo/sleepminder))提供，本项目将重构先前源码，并以其为基础增添功能。



@Sopamo:

> *Disclaimer: This application has been written in 2014 and the android code might be quite outdated now. However, the bachelor thesis still provides some interesting insight into sleep monitoring.*
>
> A sleep monitoring application for Android. Includes a framework to create custom sleep monitoring apps. This application is a demonstration of the library's features.
>
> This framework and the demo application were developed during my bachelor thesis at the Univeritiy of Ulm: http://dbis.eprints.uni-ulm.de/1183/1/BA_Mohr_15.pdf

对代码块存疑：

`AudioView.java`

```java
        if (points2.size() > 0) {
            Double[] curr = points2.get(points2.size() - 1);
            paint.setColor(Color.RED);
            canvas.drawText("RLH: " + curr[0], 100f, 200f, paint);

            paint.setColor(Color.YELLOW);
            canvas.drawText("VAR: " + curr[1], 100f, 300f, paint);

            paint.setColor(Color.BLUE);
            // With doubt, I think this should be rms, not lux
            canvas.drawText("RMS: " + lux, 100f, 400f, paint);
```

