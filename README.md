# 🌀 Rotating ASCII Donut in Pygame

A mesmerizing real-time 3D **ASCII torus (donut)** rendered using Pygame — animated with smooth rotation, dynamic lighting, and vibrant rainbow color cycling. Inspired by Andy Sloane's legendary terminal donut, reimagined with modern visuals.

![screenshot](https://upload.wikimedia.org/wikipedia/commons/2/2e/ASCII-Donut-Demo.gif)  
*Illustrative only — actual output is rendered in a Pygame window with colors.*

---

## 🚀 Features

- ✅ 3D rotating torus using trigonometric projections  
- ✅ Dynamic color cycling using HSV → RGB conversion  
- ✅ Realistic lighting simulated via ASCII character luminance  
- ✅ Responsive Pygame rendering with customizable FPS  
- ✅ Pause/Resume animation with the `Space` key

---

## 📦 Requirements

- Python 3.x  
- `pygame`  
- Standard math and color libraries (`math`, `colorsys`, `os`)

### 📥 Install Dependencies

```
pip install pygame
```
---

## 🧠 How It Works

- The donut is generated using two nested loops over angles `theta` and `phi`, forming a parametric torus.
- Points are rotated in 3D space using rotation matrices with angles `A` (x-axis) and `B` (z-axis).
- Each 3D point is projected onto a 2D grid using perspective scaling (`K1`, `K2`).
- Brightness (`L`) is calculated per point and mapped to an appropriate ASCII character from a predefined set.
- Each character is rendered using `pygame.font` with dynamic rainbow coloring (`HSV → RGB`).
- A z-buffer ensures proper depth rendering — only the nearest character at each position is displayed.

---

## 🎮 Controls

| Key       | Action            |
|-----------|-------------------|
| `ESC`     | Exit program       |
| `SPACE`   | Pause / Resume     |
| Window `X`| Quit application   |

---

## 📸 Preview

Here’s what it looks like in action:

🌈 A rotating 3D donut made of characters, filled with colorful ASCII magic.

> ![Image](https://github.com/user-attachments/assets/ba199b1e-450b-4655-9d61-fef59611555f)
---

## 🔧 Customization

You can tweak the following variables in the code to modify the output:

| Variable        | Description                                 |
|-----------------|---------------------------------------------|
| `pixel_width`   | Size of each character's display cell (in px) |
| `theta_spacing` | Angular step around the donut tube          |
| `phi_spacing`   | Angular step around the donut ring          |
| `chars`         | ASCII characters used for brightness levels |

---

## 📜 License

This project is released under the [MIT License](LICENSE).  
Inspired by [Andy Sloane’s ASCII donut](https://www.a1k0n.net/2011/07/20/donut-math.html).

---

## 👨‍💻 Author

**Ranjeet Singh**  
BTech AI Student @ DSEU BPIBS  
Passionate about graphics, creative coding, and real-time visual systems.
