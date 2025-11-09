#  🟨 Flappy-Box.
Back when browsers were slow and games loaded in 10 seconds…
we had Flappy Bird.

This isn’t a remake.
This is Flappy Box — stripped down, rebuilt from zero, and tuned for today.
No bird. No sprites. Just a box, some pipes, and your reflexes.

Built in one file. No excuses. 

Made in **vanilla HTML5 Canvas**.  
No libraries. No assets. Just pure JavaScript, physics, and focus.

## 🎮 How to Play
- **Desktop**: Press `SPACE` or `CLICK` to jump and `R` to restart after hugging the pipe from different areas.
- **Mobile**: bruh i dont know how too cause never tested it there.You can try if you want too.
- Avoid pipes. Pass through gaps. Survive.

---

## 🛠️ How to Customize (Edit the Code!)

Everything is controlled by simple values in the `cfg` (config) object and a few key lines.  
Open the HTML file in any text editor and tweak these:

### 🕹️ Game Feel
```js
const cfg = {
  g: 0.6,        // Gravity — higher = faster fall
  jump: -8,      // Jump power — more negative = stronger jump
  pipeV: 2,      // Pipe speed — higher = faster pipes
  gap: 180,      // Vertical gap between pipes (in pixels)
  pipeW: 80      // Pipe width (in pixels)
};
```

### 🎨 Visuals

Background color: Change #70c5ce in <body> and canvas style

Bird/Box color: Edit '#ffd700' in the draw() function

Pipe color: Change '#228b22' in the draw() function

Example: Make it neon?

```js// In draw()
ctx.fillStyle = '#00ffea';  // box
ctx.fillStyle = '#ff00ff';  // pipes
```
### 📏 Size & Layout

Box size: Edit w:35, h:35 in the bird object

Score size/position: Tweak ctx.fillText(score, W/2, 60);

Start/Game Over text: Modify the strings and positions in the draw overlays

### 🚀 Advanced: Change Pipe Spacing

Pipes spawn every 100 frames. To make them closer/farther:
```js
// Find this line:
if (++frame % 100 === 0) addPipe();

// Change 100 → lower = more pipes (e.g., 70), higher = fewer (e.g., 130)
```
## 💡 Why This Exists
I built this to:

Understand real-time game loops

Master collision, input, and state management

Prove you don’t need frameworks to make something fun

It’s not perfect.

But it’s mine.

## ▶️ How to Run
Save the code as flappy-box.html

Open it in any browser

Play. Tweak. Break. Fix. Repeat.

No install. No build steps. Just code → browser → play.


## Just try not to hug the pipe 😅
