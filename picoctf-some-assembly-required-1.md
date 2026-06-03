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
