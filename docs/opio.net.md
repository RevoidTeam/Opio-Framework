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

> make custom apply oficial modes
```cs
public static void ApplyOfficialModes()
{
    OpioMode.Apply("NEW", new NEW());
    OpioMode.Apply("math", new Math());
    OpioMode.Apply("go", new GetChild());
    OpioMode.Apply("so", new SetChild());
    OpioMode.Apply("ao", new AddChild());
    OpioMode.Apply("ro", new RemoveChild());
    OpioMode.Apply("STRING", new STRING());
    OpioMode.Apply("INT", new INT());
    OpioMode.Apply("FLOAT", new FLOAT());
    OpioMode.Apply("CHAR", new CHAR());
    OpioMode.Apply("TRUE", new TRUE());
    OpioMode.Apply("FULSE", new FULSE());
    OpioMode.Apply("CLASS", new CLASS());
    OpioMode.Apply("WC", new WHITECLASS());
    OpioMode.Apply("ACTION", new ACTION());
    OpioMode.Apply("rsa", new RunSystemAction());
    OpioMode.Apply("roa", new RunOpioAction());
    OpioMode.Apply("rosa", new RunOpioSimplyAction());
    OpioMode.Apply("raa", new RunAutoAction());
    OpioMode.Apply("rc", new ReClass());
    OpioMode.Apply("info", new info());
}
```

