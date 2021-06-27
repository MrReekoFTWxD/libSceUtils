# INI

## Creating/Saving INI file
```
CSimpleIni ini;

ini.SetIntValue("Section", "Key", 1500);
ini.SaveFile("path");
```

## Read INI file
```
CSimpleIni ini;
int fromIni;

if (ini.LoadFile("path") == SCE_OK)
{
    fromIni = ini.GetIntValue("Section", "Key");    
}
```