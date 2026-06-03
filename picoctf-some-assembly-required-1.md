# picoCTF: Some Assembly Required 1

## Challenge
Web exploitation with WebAssembly. Find flag via client-side debugging.

Target: http://wily-courier.picoctf.net:49820/index.html

## What I Did

Opened DevTools (F12) → Sources panel.

Found WebAssembly module in debugger. Saw WASM bytecode handling user input.

Set breakpoint in WASM function. Ran the challenge. Debugger paused execution.

Inspected memory at breakpoint. Found flag string in plaintext.

## Flag
picoCTF{68ff4bc93f6d67637b2f471be209d132}

## Why This Works
Client-side verification in WASM is inspectable at runtime. 
Compiled code doesn't hide secrets from a debugger.

## Tools
- Firefox DevTools
- Sources panel debugger
- Breakpoint on WASM function

## Screenshots
![WASM in Sources Panel] 
<img width="1364" height="651" alt="Screenshot 2026-06-03 140113" src="https://github.com/user-attachments/assets/76a4e05f-d7dc-4d69-b70d-3a15d6c1eab7" />

![Debugger Breakpoint] <img width="978" height="801" alt="Screenshot 2026-06-03 140123" src="https://github.com/user-attachments/assets/d821245c-3bc7-439c-a299-321d9cb5e3e5" />

