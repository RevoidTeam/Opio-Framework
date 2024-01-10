# Ops-Official-Modes
Official documentation for OPS modes

> for Install in opio.net using this command in void Main :
```cs
OpioSimply.ApplyOfficialModes();
```

# Soon Docs
## soon docs for incomplete systems
> NEW, Math, SetAndAddChild

# ReClass
## run
```ops
rc>{name of white class}
```
## compiler
```cs
if (code.Split('.', ' ', '!', '#', '@', '$', '%', '^', '&', '*', '(', ')', '\"').Length == 1 && OpioEngine.oc.ContainsKey(code))
{
    Return = "rc>" + code;
}
```

# GetChild
## run
```ops
go>{object or class path}
```
## compiler
```cs
//null
```

# SetChild
## run
```ops
{add new object to SOO}
so>{object or class path}
```
## compiler
```cs
//null
```

# AddChild
## run
```ops
{add class to SOO}
{add object to SOO}
so>
```
## compiler
```cs
//null
```

# RemoveChild
## run
```ops
{add class to SOO}
so>{object ot class path}
```
## compiler
```cs
//null
```

# CHAR
## run 
```ops
CHAR>{your char}
```
## compiler
```cs
if (code.First() == '\'' && code.Last() == '\'')
{
    Return = "CHAR>" + code.Substring(1, code.Length - 2);
}
```

# STRING
## run 
```ops
STRING>{your string}
```
## compiler
```cs
if (code.First() == '\"' && code.Last() == '\"')
{
    Return = "STRING>" + code.Substring(1, code.Length - 2);
}
```

# INT
## run
```ops
INT>{your int}
```
## compiler
```cs
if (RemoveFor(code, "0123456789") == String.Empty)
{
    Return = "INT>" + code;
}
```

# FLOAT
## run
```ops
FLOAT>{your int}
```
## compiler
```cs
if (RemoveFor(code, "0123456789.") == String.Empty)
{
    Return = "INT>" + code;
}
```

# TRUE
## run
```ops
TRUE>
```
## compiler
```cs
if (code == "true")
{
    Return = "TRUE>";
}
```

# FALSE
## run
```ops
FALSE>
```
## compiler
```cs
if (code == "false")
{
    Return = "FALSE>";
}
```

# ACTION
## run
```ops
ACTION>{your actions}
```
## compiler
```cs
if (code.StartsWith('{') && code.EndsWith('}'))
{
    code = code.Remove(0, 1);
    code = code.Remove(code.Length - 1, 1);
    Return = "ACTION>" + code.Replace("~", "|~|");
}
```

# CLASS
## run
```ops
CLASS>{class name}
```
## compiler
```cs
if (code.StartsWith("class "))
{
    code = code.Remove(0, 6);
    Return = "CLASS>" + code;
}
```

# WHITECLASS
## run
```ops
{get your class in SOO}<
WC>
```
## compiler
```cs
if (code == ":static")
{
    code.Remove(0, 6);
    Return = "WC>";
}
```

# info
## run
```ops
info>
```
## compiler
```cs
if (code[0] == '/' && code[1] == '/')
{
    Return = "info>" + code.Remove(0, 2);
}
```

# auto go> for null if
# compiler
```cs
Return = "go>" + code.Replace('.', '/');
```
# RunAction
## compiler
```cs
if (code.Contains('(') && code.Last() == ')')
{
    List<string> actvar = code.Split('(').ToList();
    string path = actvar[0].Replace('.', '/');
    string var = actvar[1];
    actvar.RemoveAt(0);
    actvar.RemoveAt(0);
    foreach (string svar in actvar)
    {
        var += "(" + svar;
    }
    var = var.Remove(var.Length - 1);

    path = "<go>" + path + "<raa>";

    string nv = "";
    string pattern = ",(?![^(]*\\))";
    List<string> substrings = Regex.Split(var, pattern).ToList();
    substrings.Reverse();
    foreach (string m in substrings)
    {
        nv += opsCompiler(m)+"<";
    }
    Return = nv + path;
}
```
