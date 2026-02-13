# key2noise1.1
key2noise 1.1 is a Python tool designed to manipulate raw files to create complex textures and rhythms  

Description:
Real-time audio processing tool with two audio pools, accumulator/direct processing, percussive engine, and reverb. GUI based on Tkinter with drag-and-drop support.

Dependencies:
Install Python 3.10+ and required packages:
pip install numpy sounddevice tkinterdnd2
- numpy: numerical processing
- sounddevice: audio I/O
- tkinterdnd2: drag-and-drop GUI
- tkinter: included with Python on macOS

Keyboard Controls:
r: Adjust rate
l: Adjust level
y: Adjust acc_decay
f: Adjust fb_amt
s: Adjust speed
a: Adjust alpha
d: Adjust delay
w: Adjust smooth
x: Adjust dist
u: Adjust comb_con
i: Adjust comb_fb
0: Randomize all parameters & reset buffers
+: Toggle engine mode (DIRECT / ACCUMULATOR)
7: Randomize percussive geometry
8: Randomize percussive morphology
9: Next percussive file
n: Next file in pool 1
ù: Stop pool 1

GUI Controls:
LOAD 1 / STOP 1 / NEXT 1: control main audio pool
LOAD 2 / STOP 2 / NEXT 2: control percussive pool
Log box: shows key presses, parameter updates, and pool info

Notes:
Adjust blocksize in recreate_stream(blocksize) to optimize CPU load vs. audio responsiveness.
Audio files should be raw .u8 (unsigned 8-bit PCM) for pool loading.
