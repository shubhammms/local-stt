# local-stt

Lightweight background speech-to-text for Windows and macOS.

Press **Ctrl+Shift+Space** to start recording, press again to stop — your transcription is copied to the clipboard instantly.

Runs silently in the system tray. Uses [faster-whisper](https://github.com/SYSTRAN/faster-whisper) (tiny model, ~75 MB) — no PyTorch, no cloud, no account.

---

## Download

Go to the [Releases](../../releases) page and download the latest build for your platform.

### Windows
1. Download `local-stt.exe`
2. Run it — it appears in your system tray
3. Press **Ctrl+Shift+Space** to record

### macOS
1. Download `local-stt-mac.zip` and extract it
2. Move `local-stt.app` to your Applications folder
3. Launch it — it appears in your menu bar
4. On first launch, allow Accessibility access when prompted:
   **System Settings → Privacy & Security → Accessibility → local-stt → enable**
5. Press **Ctrl+Shift+Space** to record

> The Accessibility permission is required for the global hotkey to work across all apps.

---

## Usage

| Action | Result |
|---|---|
| `Ctrl+Shift+Space` | Start recording |
| `Ctrl+Shift+Space` again | Stop & transcribe |
| `Esc` | Dismiss result overlay |

Transcribed text is automatically copied to your clipboard.

---

## Run from source

```bash
git clone https://github.com/YOUR_USERNAME/local-stt
cd local-stt
python -m venv venv
# Windows:
venv\Scripts\activate
# macOS:
source venv/bin/activate

pip install -r requirements.txt
python app.py
```

## Build yourself

**Windows:**
```
build_windows.bat
```
Produces `dist\local-stt.exe`

**macOS:**
```bash
chmod +x build_mac.sh && ./build_mac.sh
```
Produces `dist/local-stt-mac.zip`

---

## Privacy

Everything runs locally. No audio, text, or data ever leaves your machine.
