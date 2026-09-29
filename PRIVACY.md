# Layerdeck: privacy policy

Last updated: 30 September 2026

Layerdeck is a Stream Deck plugin that runs entirely on your own PC.

**What it reads.** Layerdeck connects only to Affinity's own local MCP server on the same computer (`http://[::1]:6767`, a loopback address that other computers can't reach). It reads the state of the open Affinity document: its title and unsaved status, the undo history's step names and position, the number of snapshots, and the selected layer's name, opacity, blend mode, visibility, lock, size, position and fill colour. It shows these on your Stream Deck.

**What it changes.** Only what you ask for with a key or dial (for example a layer's opacity, the selection, a snapshot, an export or a script you chose).

**What it sends.** Nothing leaves your PC. Layerdeck has no servers, no accounts, no analytics and no telemetry. It doesn't upload, copy or keep your documents. Quick Export writes files only to the folder you choose on your Desktop. Run Script sends the script file you chose to Affinity on the same PC.

**Windows helper.** A small PowerShell helper that ships with the plugin checks whether Affinity is the active window (so Layerdeck refreshes faster while you work in Affinity) and presses shortcuts in Affinity when you use a Tool, Document or Brush Size key. It doesn't read keystrokes, files or other apps.

**Logs.** The Stream Deck app keeps a local plugin log (connection status and errors, no document contents) in the plugin's folder. It stays on your PC.

**Removing Layerdeck.** Uninstall the plugin in the Stream Deck app. To close Affinity's MCP server, turn off Edit ▸ Settings ▸ Model Context Protocol ▸ Enable Affinity MCP.

**Contact.** Open an issue at https://github.com/ChympyJames/layerdeck/issues.
