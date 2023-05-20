# LEGO Spike Hub and the Light Matrix

A Python snippet utilizing the LEGO Spike light matrix, [MicroPython](https://lego.github.io/MINDSTORMS-Robot-Inventor-hub-API/), and a variety of commands: `set_pixel()`, `show()`, `show_image()`, and `play_animation()`.

```py
from mindstorms import MSHub
from mindstorms.control import wait_for_seconds
import math

hub = MSHub()

hub.light_matrix.set_pixel(0, 0, 100)

wait_for_seconds(1)

pixels = '99999:96669:96669:96669:99999'
hub.light_matrix.show(pixels)

wait_for_seconds(1)

hub.light_matrix.show_image('HAPPY')

wait_for_seconds(1)

hub.light_matrix.show_image('ASLEEP')

wait_for_seconds(1)

anim_countdown = [
    '09990:09000:09990:00090:09990',
    '09090:09090:09990:00090:00090',
    '09990:00090:09990:00090:09990',
    '09990:00090:09990:09000:09990',
    '00900:09900:00900:00900:09990',
    '99999:99999:99999:99999:99999'
]

hub.light_matrix.play_animation(anim_countdown, 1, 'slide right', True)

hub.light_matrix.off()

print("Program complete")
```

***

## Repo Resources

* [Visual Studio Code](https://code.visualstudio.com/)
* [MicroPython for LEGO Robot Inventor](https://www.lego.com/en-ca/themes/mindstorms/downloads)
* [LEGO Mindstorms](https://www.lego.com/en-ca/themes/mindstorms)
* [LEGO Mindstorms App for Mac](https://apps.apple.com/us/app/lego-mindstorms-inventor/id1515448947)
* [LEGO Mindstorms App for Android](https://play.google.com/store/apps/details?id=com.lego.retail.mindstorms)
* [LEGO Mindstorms App for Windows](https://www.microsoft.com/store/apps/9N7GN3KC2GK6)

<a href="https://codeadam.ca">
<img src="https://codeadam.ca/images/code-block.png" width="100">
</a>
