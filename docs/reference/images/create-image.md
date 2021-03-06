# Create Image

Make an [image](/makecode-blockeditor/reference/images/image) (picture) for the @boardname@
[LED screen](/device/screen).

```sig
images.createImage(`
. . # . .
. # # # .
# # # # #
. # # # .
. . # . .
`)
```

## Parameters

* ``leds`` is a [string](/types/string) that says which LEDs
on the screen should be on and which should be off.

## Example: Flip-flopping arrow

If you press button `A`, this program will make a picture of an
arrow and show it on the LED screen. If you press button `B`, the
program will show a picture of the arrow upside-down.

```blocks
input.onButtonPressed(Button.A, () => {
    images.createImage(`
        . . # . .
        . # # # .
        # . # . #
        . . # . .
        . . # . .
        `).showImage(0);
});
input.onButtonPressed(Button.B, () => {
    images.createImage(`
        . . # . .
        . . # . .
        # . # . #
        . # # # .
        . . # . .
        `).showImage(0);
});
```

## See also

[image](/makecode-blockeditor/reference/images/image),
[create big image](/makecode-blockeditor/reference/images/create-big-image),
[show image](/makecode-blockeditor/reference/images/show-image),
[scroll image](/makecode-blockeditor/reference/images/scroll-image), [show animation](/makecode-blockeditor/reference/basic/show-animation)

