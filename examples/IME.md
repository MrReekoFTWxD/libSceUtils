#IME

## Keyboard
```
char keyboardBuffer[0x400]; 

//ConverToWChar comes from libSceUtils/string.h
sceImeKeyboard(keyboardBuffer, "Keyboard Title", ConvertToWChar("Text In the input by default"));
```

## Dialog
```
sceMessageDialog("Message In Dialog);
```