## Copying / Pasting

- `y[motion]` saves text in `"` and `0` registers
- `d[motion]` deletes the text you want to replace ( saved to `"` register)
- `"0p` Paste the yanked text

-  `"cyy` Copy  a line to registry "c" ( copy a word would be `"cyaw"`)
- `"cp` Paste a line from registry "c"
- `"+p` Paste from system clipboard (Linux)
- `:reg` List all defined register types