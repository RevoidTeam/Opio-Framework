# Opio Framework 🖼️
It is an integrated framework for making some applications, testing and making simple applications. This framework was created for the purpose of fun for YouTube and in order to use it with a browser specific to this language only, and does not require known languages ​​such as html, css, js, and these sites only work on a browser. OP
> [!CAUTION]]
> all Opio Framework in developer mode.


# Install ☑️
## opio.net
for install [opio.net](https://github.com/RevoidTeam/Opio-Framework/tree/main?tab=readme-ov-file#opionet-) you can install from nuget.org :
https://www.nuget.org/packages/opio.net or run this command in PM :
```PowerShell
NuGet\Install-Package opio.net -Version 1.0.0
```
## opio framewok
for install opio framework you can install from releases :
> [!WARNING]
> Opio Framework installer coming soon.

# Opio 📦
Opio is a new programming language designed for the modern era 👨‍💻. It has been developed to be multilingual, allowing programmers to write code in any language they prefer, including Arabic. In addition, Opio supports visual programming, making it ideal for users who prefer a visual interaction with their code.

## "Hello World" Example in Opio
![opioAD](https://github.com/RevoidTeam/Opio-Framework/assets/155166369/b46b4316-d40f-45ed-b01d-d5fe99e14b42)

## Features 🥇
- Multilingual support 📚
- Translation of op files to ops 🗄️
- Execution of .ops files 📂
- [Integrated editor 🍎](https://github.com/RevoidTeam/Opio-Framework/tree/main?tab=readme-ov-file#opeditor-%EF%B8%8F)
- Visual programming 💳
- Speed of translation and execution 🚅
- Ambitious goals 🥅

## Getting Started
![gss](https://github.com/RevoidTeam/Opio-Framework/assets/155166369/72d5dc58-d2a7-4103-b7de-d88021c0e788)

## Basic Applications 🗃️
- Console Applications 💬
- Oeb.OPS 🕸️
> [!TIP]
> Opio Graphics app in developer mode. 

## How work
![opioAD2](https://github.com/RevoidTeam/Opio-Framework/assets/155166369/ce8e2ec3-565c-4edd-b89a-fde60b5b9669)

## Classes 🏛️
- **OpioEngine**: A class in the .net project that runs ops files. It previously ran ops files without translation, and this feature may return.
- **OpioMode**: A class that runs only one Mode.OPS and some of them compile from an op file.
- **OpioSimply**: It is the basic translator from op to ops.
- **OpioTask**: Some tools used for testing and some other things.
- **OpioSimplyAction, OpioAction, OpioClass**: Operating systems for testing.
- **OpioConsole**: To support Class Console in ops, op.
- **OpioTranslator**: Multilingual translator.

## Translation from op to ops 💽
The tool works by separating each command individually. It uses the OpioMode system to send the untranslated code, then performs the custom translation of every single thing after identifying it and builds an integrated code.
> [!IMPORTANT]
> you can Translation from op to ops in opio.net with `OpioSimply.opsCompiler({your op code})`.

# OpEditor 🎙️
OpEditor is a unique programming editor designed for the Opio programming language. It supports both textual and visual programming, and includes a translator and an operator for the Opio language.

## Features

- **Textual and Visual Programming**: Write code in text format or manipulate program elements graphically.
- **Op to Ops Translation**: Translate code written in Op (standard mode) into Ops (simpler mode).
- **Extraction for All Systems**: Extract a complete project for an application on all systems.
- **EXE Support**: Currently, the [editor](https://github.com/RevoidTeam/Opio-Framework/tree/main?tab=readme-ov-file#opeditor-%EF%B8%8F) only supports the creation of `.exe` files for Windows systems.

# Supports 🔥
![linkyt](https://github.com/RevoidTeam/Opio-Framework/assets/155166369/5d90d091-470a-450f-86bb-81f29c951a7c)

# opio.net 🌏
[Install opio.net](https://github.com/RevoidTeam/Opio-Framework/tree/main?tab=readme-ov-file#opionet) 
> A sample project for running user commands
> name spaces
```cs
using opio;
using opio.packages;
```
> Main void
```cs
OpioConsole.Using();
OpioFiles.Using();
OpioSystem.Using();
OpioSimply.ApplyOfficialModes();
```
> and (app)
```cs
OpioEngine.BuildSimplys(OpioSimply.opsCompiler(Console.ReadLine()));
```
> or (debig)
```cs
while (true)
{
    OpioEngine.BuildSimplys(OpioSimply.opsCompiler(Console.ReadLine()));
    int i = 0;
    while (OpioEngine.oo.Count != i)
    {
        Console.WriteLine(OpioEngine.oo[0]);
        i++;
    }
}
```
> [!TIP]
> for learn opio.net or you need help go to [opio.net docs](https://github.com/RevoidTeam/Opio-Framework/blob/main/documentation/opio.net)https://github.com/RevoidTeam/Opio-Framework/blob/main/documentation/opio.net
