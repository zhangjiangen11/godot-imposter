# Godot Imposter
Imposter plugin for Godot 4.x

Simple implementation of octahedral impostors in Godot.

## About
This project was inspired by: https://github.com/wojtekpil/Godot-Octahedral-Impostors

Unfortunately, the project has not been adapted for Godot 4. Godot 4.x introduces significant architectural changes compared to 3.x, rendering the original project incompatible.

Based on the original work, and considering Godot 4.x's features along with my understanding of impostor techniques, I have developed a version compatible with Godot 4.x.

Special thanks to the original author. I reused and adapted their shader code specifically for Godot 4.x.

**Verified compatibility: Godot v4.5.beta5**

---

## Major Updates
1. **Disabled batch processing**
2. **New editor integration** — The plugin is now accessible via the 3D editor viewport instead of a bottom panel.

---

## Usage
When selecting a node (or its child nodes) inherited from `GeometryInstance3D` in the Scene Tree, an **Imposter** button will appear in the 3D editor toolbar, adjacent to *Transform* and *View* controls.

![image](https://github.com/zhangjt93/godot-imposter/blob/master/guide/20250815185643_157.png)

### Steps:
1. Select a node containing `GeometryInstance3D` elements in the Scene Tree
2. Locate the **Imposter** button in the 3D editor toolbar
3. **Click to open the configuration window**

---

## Important Notes
⚠️ **Transform Warning**:
If baking a node with world-space transformations (e.g., scaled/rotated objects), the **node's transform** will be reset during baking.

**Workaround**:
Place transformed nodes under a `Node3D` parent, then:
1. Reset the **parent node's transform** to zero
2. Bake the parent node while preserving children transforms

---

## Roadmap
Researching texture compression methods to optimize memory usage and performance while preserving visual fidelity. Priority for next updates.

---

## Support
- 🐞 **Issues?** Open a GitHub ticket or contact me directly
- 💡 **Suggestions?** Feedback and ideas are welcome!
- ⭐ **Enjoy this tool?** Star the repo to support development!

---

## License
MIT License. See [LICENSE](LICENSE) for details.

