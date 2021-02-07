# AudioVisualizer
An audio visualizer for Roblox

https://devforum.roblox.com/t/audio-visualizer-bars/1032002/1

The usage is super easy. The module takes care of basically everything for you. You specify a bar amount, and the module will automatically determine the sampling rate and bar falloff for you.

## API:

```Lua
function VisualizerModule.new(Frame, BarCount)
```
*Creates a new visualizer*

`Frame: Instance` The GuiObject the bars will be put in
`BarCount: number` How many bars the visualizer should use

**returns** a `Visualizer`
.

```Lua
function Visualizer:LinkToSound(Sound)
```
*Makes the visualizer display the given Sound*

`SoundObject: Instance` The sound to visualize

**returns** void
.

```Lua
function Visualizer:UnlinkFromSound()
```
*Makes the visualizer stop displaying the currently linked sound*

**returns** void

.

```Lua
function Visualizer:Destroy()
```
*Cleans up the visualizer*

**returns** void

----

## Usage:

APIs are sometimes hard to understand without an example, so here you go. It really is simple.

```Lua
local VisualizerModule = require(script.Visualizer)

local Visualizer = VisualizerModule.new(GuiFrame, 80)
Visualizer:LinkToSound(script.Music)

script.Music:Play()
```

----

## Demo:

Here's a demo of various bar counts: (YouTube cuz file is way too large to embed directly)

https://www.youtube.com/watch?v=NY3pTvmlG24

-----

## Source:

https://www.roblox.com/library/6360148029/Visualizer
