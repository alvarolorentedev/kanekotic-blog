---
title: C# - Paths to system folders
date: 2016-01-29 20:22:36
tags: daily, learn
---

In the Environment class there is a property called SpecialFolder. This will provide the paths to folders like: Program files, desktop, AppData, etc. The use is the next one:

```csharp
Environment.SpecialFolder.<NameSpecialFolder>
```

Where <NameSpecialFolder> is the given name of the folder required, for example the AppData Local folder will be

```csharp
Environment.SpecialFolder.LocalApplicationData
```
