# libSceUtils
PS4 prx library with some useful additions

## Needed
- Visual Studio 2015+
- Sony PS4 4.00 SDK or newer

## Installation
  1. Download the latest release from Release
  2. Put libSceUtils.a in `C:\Program Files (x86)\SCE\ORBIS SDKs\4.000\target\lib\`
  3. Put SceUtils folder in `C:\Program Files (x86)\SCE\ORBIS SDKs\4.000\target\include`
  4. Add `#include <SceUtils\SceUtils.h>` into your project

### Features
- System
  - File Systems
    - Write/Read File
    - Make Directory
    - Check if file/directory Exist
  - Notification
    - Notication with Custom icon (Provided from https://github.com/OSM-Made/PS4-Notify)
  - IME
    - Keyboard
    - Dialog
- INI
  - Create/Read INI files
- Strings
  -  va
  -  char* to wchar*
- Detours
  - Hooking/Restoring for sprx projects
- vec/vec2/vec3/vec4
