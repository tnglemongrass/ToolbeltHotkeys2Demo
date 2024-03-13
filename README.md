# ToolbeltHotkeys2Demo

This project contains a minimal example to reproduce a possible bug in the Toolbelt Hotkeys2 library.

Actual behavior: In a Maui Blazor Hybrid App, Hotkeys2 shows an error/warning on startup (the app runs fine and hotkeys work):

```
Toolbelt.Blazor.HotKeys2.HotKeys: Error: Could not find 'Toolbelt.Blazor.getProperty' ('Toolbelt' was undefined).
Error: Could not find 'Toolbelt.Blazor.getProperty' ('Toolbelt' was undefined).
    at https://0.0.0.0/_framework/blazor.webview.js:1:540
    at Array.forEach (<anonymous>)
    at l.findFunction (https://0.0.0.0/_framework/blazor.webview.js:1:508)
    at w (https://0.0.0.0/_framework/blazor.webview.js:1:5251)
    at https://0.0.0.0/_framework/blazor.webview.js:1:3044
    at new Promise (<anonymous>)
    at g.beginInvokeJSFromDotNet (https://0.0.0.0/_framework/blazor.webview.js:1:3007)
    at https://0.0.0.0/_framework/blazor.webview.js:1:48020
    at EventTarget.<anonymous> (<anonymous>:7:62)
    at EmbeddedBrowserWebView.<anonymous> (<anonymous>:1:40673)

Microsoft.JSInterop.JSException: Could not find 'Toolbelt.Blazor.getProperty' ('Toolbelt' was undefined).
Error: Could not find 'Toolbelt.Blazor.getProperty' ('Toolbelt' was undefined).
    at https://0.0.0.0/_framework/blazor.webview.js:1:540
    at Array.forEach (<anonymous>)
    at l.findFunction (https://0.0.0.0/_framework/blazor.webview.js:1:508)
    at w (https://0.0.0.0/_framework/blazor.webview.js:1:5251)
    at https://0.0.0.0/_framework/blazor.webview.js:1:3044
    at new Promise (<anonymous>)
    at g.beginInvokeJSFromDotNet (https://0.0.0.0/_framework/blazor.webview.js:1:3007)
    at https://0.0.0.0/_framework/blazor.webview.js:1:48020
    at EventTarget.<anonymous> (<anonymous>:7:62)
    at EmbeddedBrowserWebView.<anonymous> (<anonymous>:1:40673)
   at Microsoft.JSInterop.JSRuntime.InvokeAsync[TValue](Int64 targetInstanceId, String identifier, Object[] args)
   at Toolbelt.Blazor.HotKeys2.HotKeys.GetJsModuleAsync()
```

Expected behavior: There should be no errors on startup.

The project was created using
- Visual Studio 2022 and
- a new ".NET MAUI Blazor Hybrid App" with .NET 8.0
- following instructions on https://github.com/jsakamoto/Toolbelt.Blazor.HotKeys2

See the git commit diff for the exact changes.
