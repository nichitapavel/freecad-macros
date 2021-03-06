# freecad-macros
Personal freecad-macros

Macros default path:
- Windows: `C:\Users\<user>\AppData\Roaming\FreeCAD\Macro\`
- Linux: `/home/<user>/.FreeCAD/Macro/`

**Note 1:** is possible that _Macro_ folder does not exists.
**Note 2:** is possible the default path is without `Macro` at the end.

Linking (linux commands)
========================
- Check macro directory:
```bash
if ! [ -e ~/.FreeCAD/Macro ]; then mkdir ~/.FreeCAD/Macro; fi
```

- Make symbolic links to FreeCAD Macro path,  
with `parallel` or `for`:
```bash
parallel ln -s ${PWD}/{} ~/.FreeCAD/Macro/{/} ::: *.FCMacro
```
```bash
for macro in ./*.FCMacro; do ln -s ${PWD}/${macro} ~/.FreeCAD/Macro/.; done
```
