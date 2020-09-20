Before use, don't forget to copy AmosProAGA_System/AmosProAGA.library into S:
And Amos Pro configuration from AmosProAGA_System:S to S:

******************************************************************** 2020.09.20
- Added new method "Get Aga Palette INDEX" to get current screen color palette
- Added new method "Save Aga Palette FILE$, INDEX" to save an AGA palette stored in memory


******************************************************************** 2020.09.19
- Added new method "Load Aga Palette FILE$, INDEX" to load an IFF/ILBM CMAP file from disk
- Added new method "Set Aga Palette INDEX" To update current screen + Global Aga Palette with the one defined in the Aga Palette INDEX


******************************************************************** 2020.09.18
- Work in progress on method : "load Aga Palette FILE$, Index"


******************************************************************** 2020.09.17
- Added new method "=Rgb24( Red8, Green8, Blue8 )" to return full RGB24 color from Red, Green and Blue 8 bits color components
- Added new method "=RgbR8( RGB24Colors )" to return Red 8 bits component from full RGB24 color
- Added new method "=RgbG8( RGB24Colors )" to return Green 8 bits component from full RGB24 color
- Added new method "=RgbB8( RGB24Colors )" to return Blue 8 bits component from full RGB24 color


******************************************************************** 2020.09.16
- Added new method "Step fade aga SPEED"
- Added new method "Fade Aga DELAY"


******************************************************************** 2020.09.12
- Identified crash location in the Accessories/Object_Editor.AMOS tool.


******************************************************************** 2020.09.11
- Added list of methods in CopperListSystem.s
- Added list of methods in Screens.s
- Fixed loading of AmosPro Help.
- Increase +AMOSPro_AGA_library_Equ.s/SwapL from 32 bytes to 40 (Added 2.l for the 2 extra bitplane to swap on Screen Swap commands.)
- Update Screen Swap to works with 8 bitplanes
- Update Double Buffer to works with 8 bitplanes


******************************************************************** 2020.09.09
- Updated +Compact.s/InSPack6 to save RGB24 bits colors instead of previously RGB12
- Updated +Compact.s/InSPack7 to save RGB24 bits colors instead of previously RGB12
- Updates +AmosProAGA_Equ.s/Packed structure to handle RGB24 bits colors instead of previously RGB12
- Updates +AmosProAGA_Equ.s/DefPal components to handle RGB24 bits colors instead of previously RGB12 ( + DefPalAga, DefPalL & DefPalAgaL )


******************************************************************** 2020.09.08
- Fixed dual playfield scroll bug that was reintroduced by some changes.
- Updated batchs aall, alib and acomp to output only required datas
- Updated C/Make_Toktable and C/Make_Labels to remove useless debug output
- AmosProAGA_lib.s/Bnk.SaveA0 updated to save up to 256 colors using RGB24
- AmosProAGA_lib.s/Bnk.Load updated to load up to 256 colors using RGB24
- AmosProAGA_lib.s/Bnk.Ric updated to get up to 256 RGB24 colors instead of RGB12 previously.


******************************************************************** 2020.09.07
- Save Iff now save RGB24 colors instead of RGB12.


******************************************************************** 2020.09.05
- Colour I,RGB12 update both High and Low color bits with the RGB12 value entered.


******************************************************************** 2020.09.04
- Fixed the color flickering on Load IFF calls.


******************************************************************** 2020.09.03
- Updated CLPopulate to consider 2nd RGB12 Color palette for registers 032-255
- Fix 'Set Rgb24 Colour I, RGB24Value'


******************************************************************** 2020.08.31
- Fixed Object Editor 'unpack' command that was trashed due to new upack method in the AmosPro_Compact.lib
- Updated internal EcSCol (Colour I,RGBValue) to be able to set both color capabilities RGB12->RGB24 and RGB24->RGB24
- Colour I,RGB12 now fill both Upper and lower bits with the RGB12 value for smoother RGB12 shading
- Added 'Set Rgb24 Colour COLORINDEX,RGB24VALUE' command to AmosPro_AgaSupport.lib extension.
- fixed insertAGAColorsInCopper as it didn't insert AGA colors 032-0255 Lower 12 Bits correctly in the copper list.


******************************************************************** 2020.08.30
- Finalized Copper list support for full RGB 24 color palette for both global colors 032-255 and each screen colors 001-031.
- Load Iff now support fully RGB24 Color palette decoding and insertion in screen color palette datas
- Finalized HAM8 Support with full RGB24 Color palette support


******************************************************************** 2020.08.26
- +w.s/IffBODY improvements for HAM8 Support. 24Bits RGB Backing Store (DPaintV) not supported.
- +AmosProAGA_lib.s/IffBODY improvements for HAM8 Support. 24Bits RGB Backing Store (DPaintV) not supported.
- ++AmosProAGA_lib.s/IffScreen improvements for HAM8 Support. 24Bits RGB Backing Store (DPaintV) not supported.


******************************************************************** 2020.08.25
- Completed RGB24 Color support for SetPalette and Copper List colors update
- Continuation of AmosProAGA.library.s file component separation into several files.


******************************************************************** 2020.08.18
- Started AmosProAGA.library.s file component separation into several files.


******************************************************************** 2020.08.13
- +w.s/insertAGAColorsInCopper Updated to handle RGB24 bits colors data instead of RGB12 bits, in copper list
- +wequ.s/globAgaPalL Added for lower bits of AGA color palette
- +lEqu.s/EcScreenAGAPalL added for lower bits AGA Colors screen palette 032-255
- +lEqu.s/EcPAlL added for lower bits AGA colors screen palette 000-031
- +w.s/EcCree Updated to define RGB24 bits color palette instead of original RGB12 one
- +lib.s/IffPal Updated to get full RGB24 bits color palette from an AGA palette.
- +w.s/EcCopHo Updated to handle RGB24 bits color palette for default 000-031 screens colors


******************************************************************** 2020.08.12
- +lib.s/prepareHam8Logic method created for bitplanes list 'EcHam8Logic' to use for normal/Ham8 mode instead of default 'EcLogic' one.
- +lib.s/IffBODY update to support HAM8 mode (add support for all IFF/ILBM loading (image/anim) for HAM8 mode)


******************************************************************** 2020.08.11
- +w.s/ScSwap (ScreenSwap) updated to use the HAM8 +2 bitplanes rolling method
- +w.s/ScSwapS (ScreenSwapAll) updated to use the HAM8 +2 bitplanes rolling method
- +w.s/EcCree (CreateScreen) updated to use the HAM8 +2 bitplanes rolling method
- +w.s/EcCree (CreateScreen) updated to handle HAM8 mode in all resolutions.
- +w.s/TAbk2 (autoback2) updated to use the HAM8 +2 bitplanes rolling method
- +w.s/TAbk3 (autoback3) updated to use the HAM8 +2 bitplanes rolling method
- +w.s/EcSHam8BPLS Created to make the +2 bitplanes rolling for HAM8 mode


******************************************************************** 2020.08.10 Bob Get & Color Palette
- +AmosProAGA_lib.s/InSaveIff1-2 (SaveCMAP) : Updated to save up to 256 colors in IFF/ILBM files
- Checked many Amos Professional 2.0 commands to check compatibility with Amos Professional AGA version.
- Fixed the AMOS/WB switcher issue


******************************************************************** 2020.05.15 Bob Get & Color Palette

- +AmosProAGA_lib.s/IffPal : Updated to handle 'AGAP' + ColourCount.w palette when more than 32 colors are available.
- +AmosProAGA_library.s/EcCree : Updated to integrate AGAP + ColourCount.w palette when screen is created.
- +AmosProAGA_lib.s/PalRout : Updated to handle 'AGAP' + ColourCount.w palette when more than 32 colors are available.
- +AmosProAGA_lib.s/GSPal : Updated to handle 'AGAP' + ColourCount.w palette when more than 32 colors are available.
- +AmosProAGA_lib.s/Bnk.SaveA0 (SB_Icon, SB_Bob, SP_Sp) : Save Sprite/Icon Bank updated to handle AGAP + ColourCount.w palette when saving to file.
- +AmosProAGA_lib.s/Bnk.Load ( LB_Icons, LB_Sprites ) : Load Sprite/Icon bank updated to handle AGAP + ColourCount.w palette when available in the file.
- Save Sprites/Bobs/Icons banks now save banks using "AGAP" mode with up to 256 colors (currently forced to 256 but will be dynamic in the future)
- Load Sprites/Bobs/Icons banks now detect original Amos Professional 2.0 ECS banks and Amos Professional AGA ones using "AGAP" mode with correct color palette


******************************************************************** 2020.05.14 Bob Get & Color Palette

- +AmosProAGA_lib.s/Bnk.Ric2 restored to initial state before AGA upgrade for "Get Bob" command crashes tests
- +AmosProAGA_lib.s/Bnk.Ric2 Reimplemented clean color palette support for both default ECS and new AGA.
- Fixed the Get Bob crash issue reported by Alain.Treesong
- Removed AmosPro_Personal.lib from configuration as it caused issues.


******************************************************************** 2020.05.13 AmosPro_Personal.lib Update + AmosPro AGA Pen/Color system Update.

- Update AmosPro_Personal.lib to get latest paraters from d3 (AmosPro v2+) instead of all parameters from (a3)+ (AmosPro v1)
- AmosPro_Personal.lib should not be used with new AGA System (it currently crashes). It will soonly be integrated inside the AmosPro_AgaSupport.lib
- Updated the PEN/Colors methods to be compatible with AGA 00-255 colors.
- Fixed AGA Hires SPack/UnPack example


******************************************************************** 2020.05.10 AmosPro_Personal.lib

- Update of the AmosPro_Personal.lib to fit Amos Pro v2 compliants and use new AGA includes automatically
- Added a new script 'aext2' to compile third party extensions and copy them directly in the AmosProAGA_System:APSystemAGA/ folder (without including them in the config)
- Added the AmosPRO_Personal.lib to the new 'aext2' script
- Remain to do : Update data get from AmosPro (old v1 used to load everything from (a3)+ and new v2+ put latest value into D3))+ en APv1.
- Update AmosPro text drawing color system to be compatible with 256 colors (instead of 207 max due to a value shifting by +48 in bytes).


******************************************************************** 2020.05.07-08 Reinject previous Changes.

- Reincluded all changes for +w.s -> +AmosProAGA_library.s
- Reincluded all changes for +lib.s -> +AmosProAGA_lib.s
- Reincluded all changes for +Ilib.s -> +AmosProAGA_libI.s
- Reincluded all changes for +Equ.s -> +AmosProAGA_lib_Equ.s
- Reincluded all changes for +WEqu.s -> +AmosProAGA_library_Equ.s
- Reincluded all changes for +Edit.s -> +EditorAGA_Config.s
- Reincluded all changes for +Interpreter.s -> +InterpreterAGA_Config.s
- Reincluded Extensions/+AgaSupport.s
- Reincluded all changes for Extensions/+compact.s


******************************************************************** 2020.05.04-07 Restart from source
- Project entirely restarted from source.
- Used Marc365 repository as François's one is unusable until fixing special characters issues in many source code files.
- Recompiles version to check if everything is OK
- Reinstall the stable version of AMOS Professional on AmigaHD
- Removed directory "AMOSPro Sources" as useless
- Updated compilation directory from "AMOS" to "AmosProAGA_Build"
- ADATA : Updated all Editor_Config* referencies to EditorAGA_Config* to allow both original Amos Professional and Amos Professional AGA to run on the same computer.
- ADATA : Updated all Interpreter_Config* referencies to InterpreterAGA_Config* to allow both original Amos Professional and Amos Professional AGA to run on the same computer.
- ADATA : Updated all "AMOS" referencies with "AmosProAGA_Build"
- ADATA : Updated all "APSystem" referencies with "APSystemAGA" to allow both original Amos Professional and Amos Professional AGA to run on the same computer.
- AEDIT : Updated to use new AmosProAGA_Build directory as output, instead of previous "AMOS" one.
- AW : Renamed AMOS.library to AMOSProAGA.library to allow both original Amos Professional and Amos Professional AGA to run on the same computer.
- AW : Renamed +W.s to +AMOSProAGA_library.s
- AW : Updated compilation output path from "AMOS" to "AmosProAGA_Build"
- ALIB : Updated "c/genam FROM +lib.s TO AMOS/APSystem/AMOSPro.Lib" to "c/genam FROM +AmosProAGA_lib.s TO AmosProAGA_Build/APSystemAGA/AmosProAGA.Lib"
- AMON : Updated to use new AmosProAGA_Build directory as output, instead of previous "AMOS" one.
- ATOOLS : Updated to continue to use old AmosPro 2.0 to compile the tools.
- C/MAKE_Labels.AMOS updated +ILib.s to +AmosProAGA_LibI.s
- C/MAKE_Labels.AMOS updated +ILib_Size.s to +AmosProAGA_LibI_Size.s
- C/MAKE_Labels.AMOS updated +ILib_Functions.s to +AmosProAGA_LibI_Functions.s
- C/MAKE_Labels.AMOS updated +lib.s reference to AmosProAGA_Lib.s
- C/MAKE_Labels.AMOS updated +LEqu.s to +AmosProAGA_Lib_Equ.s
- C/MAKE_Labels.AMOS updated +Lib_Size.s to +AmosProAGA_Lib_Size.s
- C/MAKE_Toktable.AMOS updated +lib.s reference to AmosProAGA_Lib.s
- Renamed +WEqu.s to +AMOSProAGA_library_Equ.s
- +AMOS_Includes.s : Updated +WEqu.s reference to +AmosProAGA_Library_Equ.s
- +B.s : Updated referencies to AMOS.library with AMOSProAGA.library
- +B.s : Updated referencies to AMOSPro_Interpreter_Config with AMOSProAGA_Interpreter_Config
- +B.s, +Editor_Config.s : Updated AMOSPro_System: to AMOSProAGA_System:
- +B.s, +Editor_Config.s  : Updated AMOSPro_Accessories: to AMOSProAGA_Accessories:
- +B.s, +Editor_Config.s, +Interpreter_Config.s : Updated AMOSPro_Productivity1: to AMOSProAGA_Productivity1:
- +B.s, +Editor_Config.s  : Updated AMOSPro_Productivity2: to AMOSProAGA_Productivity2:
- +B.s, +Editor_Config.s  : Updated AMOSPro_Tutorial: to AMOSProAGA_Tutorial:
- +B.s, +Editor_Config.s  : Updated AMOSPro_Examples: to AMOSProAGA_Examples:
- +B.s, +Editor_Config.s  : Updated AMOSPro_Compiler: to AMOSProAGA_Compiler:
- +B.s, +Editor_Config.s  : Updated AMOSPro_Extras: to AMOSProAGA_Extras:
- +Editor_Confis.s, +Interpreter_Config.s : Updated AMOSPro_Accesories: with AMOSProAGA_Accessories
- +Editor_Config.s, +Interpreter_Config.s : Updated AMOSPro_Help with AMOSProAGA_Help
- +Editor_Config.s : Updated AMOSPro_Help.AMOS with AMOSProAGA_Help.AMOS
- +Editor_Config.s : Updated Interpreter_Config.AMOS with InterpreterAGA_Config.AMOS
- +Editor_Config.s : Updated Editor_Config.AMOS with EditorAGA_Config.AMOS
- +Editor_Config.s : Updated AMOSPro.Lib with AMOSProAGA.Lib
- Extensions/ACOMPACT : Updated to compile to new "AmosProAGA_Build/APSystemAGA" directory instead of previous "AMOS/APSystem"
- Extensions/AIO : Updated to compile to new "AmosProAGA_Build/APSystemAGA" directory instead of previous "AMOS/APSystem"
- Extensions/AMUSIC : Updated to compile to new "AmosProAGA_Build/APSystemAGA" directory instead of previous "AMOS/APSystem"
- Extensions/AREQUEST : Updated to compile to new "AmosProAGA_Build/APSystemAGA" directory instead of previous "AMOS/APSystem"
- Compiler/ACDATA : Updated to compile to new "AmosProAGA_Build" directory instead of previous "AMOS"
- Compiler/ACLIB : Updated to compile to new "AmosProAGA_Build" directory instead of previous "AMOS"
- Compiler/ACOMP : Updated to compile to new "AmosProAGA_Build" directory instead of previous "AMOS"
- Compiler/ACOMPEXT : Updated to compile to new "AmosProAGA_Build" directory instead of previous "AMOS"
- Compiler/AHEADER : Updated to compile to new "AmosProAGA_Build" directory instead of previous "AMOS"
- Kept old AmosPro version in a specific directory to uses it to recompiles aTools with classic AMOS
- Compilation Successfull
- Reconstruction of a full version for future Amos Professional AGA releases.
- AmosProAGA tests : Functionnal.
- Renamed +CEqu.s to +AmosProAGA_CEqu.s
- Renamed +Equ.s to +AmosProAGA_Equ.s
- Renamed +Debug.s to +AmosProAGA_Debug.s
- Updated +AMOS_Includes.s to +CEqu.s, +Equ.s and +Debug.s names changing.
- Updated +EditorAGA_Config.s to mention Official Francois Lionet MIT Licence terms + Link for the official GitHub repository.
- +B.s : Renamed to +AmosProAGA_Loaders.s
- APRO : Updated +B.s for name changing.
- +Monitor.s : Renamed to : AmosProAGA_Monitor.s
- AMON : updated +Monitor.s for name changing.
- +Edit.s : Renamed to AmosProAGA_Editor.s
- AEDIT : updated +Edit.s for name changing.
- +CLib.s : renamed to AmosProAGA_CLib.s
- +Version.s : Renamed to +AmosProAGA_Version.s
- +Verif.s : Renamed to +AmosProAGA_Verif.s
