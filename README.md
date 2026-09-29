# Layerdeck: support

Layerdeck is a Stream Deck plugin for **Affinity by Canva**. Its dials show the selected layer's real opacity, blend mode, name and undo history and change them as you turn; its keys show your document's save status and give you snapshots, one-press export, colour swatches, scripts and tools. It's available on the [Elgato Marketplace](https://marketplace.elgato.com).

This repository contains **documentation and support only**. Please read the [support policy](SUPPORT.md) before opening an issue. Privacy: [PRIVACY.md](PRIVACY.md).

## Set up
Layerdeck talks to Affinity through Affinity's own built-in connection, the **Model Context Protocol (MCP)** server. It is off by default. You switch it on once:

1. Install **Affinity 3.3 or newer** (Help ▸ About shows the version) and Layerdeck from the Elgato Marketplace (Windows 10/11, Stream Deck 7.1 or newer).
2. In Affinity: **Edit ▸ Settings ▸ Model Context Protocol ▸ Enable Affinity MCP**. Affinity asks to restart: choose **Yes**.
3. In the same Settings window: **Scripting ▸ Enable Affinity Scripting**.
4. Open a document and select a layer. The keys and dials come alive.

That's all. There is nothing to install into Affinity and no command to paste. The permission switches below "Enable Affinity MCP" (Desktop files, networks, saved scripts, Canva AI) can stay **off**. Only **Quick Export** needs **Access files on your Desktop** (Affinity asks you to confirm; no restart).

Until the connection works, the first Layerdeck key shows **SET UP** (amber) and pressing it opens this page. Open any Layerdeck key's settings in the Stream Deck app to see a checklist that ticks itself off live, and a **Test connection** button.

**Stream Deck +:** Layerdeck installs a ready-made **Layerdeck** profile (Opacity, Blend Mode, Layer and History dials, plus eight keys). Pick it in the Stream Deck app, or use **Load the Layerdeck profile** in any key's settings. **Other models:** drag the keys you want from the Layerdeck category.

## Actions
| Action | What it does |
|---|---|
| Opacity Dial | Shows the selected layer's opacity. Turn to change it: you see it on the canvas while you turn, and it's applied as one undo step when you stop. Push = 100 %. Touch = switch between 5 % and 1 % steps. |
| Blend Mode Dial | Shows the blend mode with the previous and next mode. Turn to preview modes live; the one you stop on is applied. Push = Normal (or apply now while previewing). Touch = cancel the preview. |
| Layer Dial | Shows the selected layer, its position (1 = top) and whether it's visible or locked. Turn = select the layer above / below. Push = show / hide. Touch = lock / unlock. |
| History Dial | Shows the last step you can undo and your position in the history. Turn = undo / redo step by step. Push = add a snapshot. |
| Size Dial | Shows the selection's size and position in pixels. Turn = scale it around its centre (preview, applied when you stop). Push = 1 % / 10 % steps. Touch = cancel. |
| Brush Size Dial | Turn to make the brush smaller or larger (Affinity's `[` and `]` shortcuts). |
| Document | The document name and a dot: orange = unsaved changes, green = saved. Press = Save, hold = Save As. |
| Snapshot | Adds a snapshot (Affinity's safe point outside the undo history) and shows how many the document has. |
| Quick Export | Exports the selection (or the whole page) as PNG, JPEG, WebP, SVG or PDF to a folder on your Desktop (default **Layerdeck Exports**) and shows the file name. |
| Run Script | Runs an Affinity script (a `.js` file you choose) in the open document and shows ✓ or the error. |
| Colour Swatch | Shows its stored colour and the selection's current fill. Press = fill the selection with it. Hold = store the selection's fill. |
| Selection Info | The selected layer's name, width × height and position in pixels. |
| Opacity Preset | Shows the layer's opacity. Press = your preset (e.g. 50 %); press again = back to 100 %. |
| Tool / Shortcut | Brings Affinity to the front and picks a tool (Move, Node, Pen, Pencil, Brush, Text, Rectangle, Zoom, Hand) or sends a command or your own shortcut. |

## FAQ
**The key says "SET UP" / "SET UP 2/2".** Step 2 (Enable Affinity MCP, then restart Affinity) or step 3 (Enable Affinity Scripting) above isn't done yet.

**The key says "Affinity".** Affinity isn't running. Press the key to start it.

**The keys are dimmed / say "Busy".** Affinity didn't answer in time (for example while it's busy exporting). Layerdeck keeps showing the last values and continues when Affinity is free.

**Quick Export says "allow Desktop".** Turn on Edit ▸ Settings ▸ Model Context Protocol ▸ **Access files on your Desktop**. Affinity only lets scripts write to your Desktop, so exports go to a folder there.

**Does turning a dial fill my undo history?** No. While you turn, Affinity shows a preview; only the value you stop on becomes one undo step, and repeated opacity changes on the same layer merge into one step (like Affinity's own slider).

**Can I use an AI assistant with Affinity's MCP at the same time?** Yes. Layerdeck and other MCP clients can be connected together.

**Tool keys pick the wrong tool.** Tool keys use Affinity's default shortcuts. If you changed them, choose "My own shortcut" in the key's settings.

**Is my artwork sent anywhere?** No. See [PRIVACY.md](PRIVACY.md).

Affinity and Canva are trademarks of Canva Pty Ltd. Layerdeck is an independent product, not affiliated with or endorsed by Canva.
