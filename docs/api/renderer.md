# renderer

## Description

Functions for drawing on the screen. Usually won't work outside the [paint](https://gamesense-docs.pages.dev/events#paint) / [paint_ui](https://gamesense-docs.pages.dev/events#paint_ui) events.

## Functions

### blur
[renderer.blur(x: number, y: number, w: number, h: number, alpha: number, amount: number)](renderer/blur.md)
> Creates a region on the screen that blurs everything behind it.

### circle
[renderer.circle(x: number, y: number, r: number, g: number, b: number, a: number, radius: number, start_degrees: number, percentage: number)](renderer/circle.md)
> Draws a filled circle on the screen

### circle_outline
[renderer.circle_outline(x: number, y: number, r: number, g: number, b: number, a: number, radius: number, start_degrees: number, percentage: number, thickness: number)](renderer/circleoutline.md)
> Draws the outline of a circle on the screen

### gradient
[renderer.gradient(x: number, y: number, w: number, h: number, r1: number, g1: number, b1: number, a1: number, r2: number, g2: number, b2: number, a2: number, direction: boolean)](renderer/gradient.md)
> Draws a horizontal or vertical gradient on the screen.

### indicator
[renderer.indicator(r: number, g: number, b: number, a: number, ...): number](renderer/indicator.md)
> Draws an indicator on the screen and returns the Y screen coordinate (vertical offset) of the drawn text, or nil on failure.

### line
[renderer.line(x1: number, y1: number, x2: number, y2: number, r: number, g: number, b: number, a: number)](renderer/line.md)
> Draws a anti-aliased line on the screen.

### load_jpg
[renderer.load_jpg(contents: string, width: number, height: number): number](renderer/loadjpg.md)
> Loads a texture from raw JPG contents (with file header). The file can for example be loaded using [readfile](g/readfile.md). Returns a texture ID that can be used with renderer.texture, or nil on failure

### load_png
[renderer.load_png(contents: string, width: number, height: number): number](renderer/loadpng.md)
> Loads a texture from raw PNG contents (with file header). The file can for example be loaded using [readfile](g/readfile.md). Returns a texture ID that can be used with renderer.texture, or nil on failure

### load_rgba
[renderer.load_rgba(contents: string, width: number, height: number): number](renderer/loadrgba.md)
> Loads a texture from a RGBA buffer. Returns a texture ID that can be used with renderer.texture, or nil on failure

### load_svg
[renderer.load_svg(contents: string, width: number, height: number): number](renderer/loadsvg.md)
> Loads a [SVG](https://developer.mozilla.org/en-US/docs/Web/SVG) from a string. The file can for example be loaded using [readfile](g/readfile.md). Returns a texture ID that can be used with [renderer.texture](renderer.md), or nil on failure

### measure_text
[renderer.measure_text(flags: string, ...): number, number](renderer/measuretext.md)
> Returns width, height. This can only be called from the paint callback.

### rectangle
[renderer.rectangle(x: number, y: number, w: number, h: number, r: number, g: number, b: number, a: number)](renderer/rectangle.md)
> Draws a filled rectangle on the screen

### text
[renderer.text(x: number, y: number, r: number, g: number, b: number, a: number, flags: string, max_width: number, ...)](renderer/text.md)
> Draws text on the screen.

### texture
[renderer.texture(texture: number, x: number, y: number, w: number, h: number, r: number, g: number, b: number, a: number, mode: string)](renderer/texture.md)
> Draws a texture from the texture id created from [load_rgba](renderer.md), [load_png](renderer.md), [load_jpg](renderer.md) or [load_svg](renderer.md)

### triangle
[renderer.triangle(x1: number, y1: number, x2: number, y2: number, x3: number, y3: number, r: number, g: number, b: number, a: number)](renderer/triangle.md)
> Draws a filled triangle on the screen. The points need to be specified in clockwise order.

### world_to_screen
[renderer.world_to_screen(x: number, y: number, z: number): number, number](renderer/worldtoscreen.md)
> Returns the screen coordinates of a world position or nil if the world position is not visible on your screen.
