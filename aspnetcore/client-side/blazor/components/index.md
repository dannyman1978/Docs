---
title: Blazor components
author: guardrex
description: Learn how to create and use Blazor components, the fundamental building blocks of Blazor apps provided by compiled Razor or C# files.
manager: wpickett
ms.author: riande
ms.custom: mvc
ms.date: 03/27/2018
ms.prod: asp.net-core
ms.technology: aspnet
ms.topic: article
uid: client-side/blazor/components
---
# Blazor components

By [Luke Latham](https://github.com/guardrex)

[!INCLUDE[](~/includes/blazor-preview-notice.md)]

A Blazor *component* represents any programming feature or collection of features that can be represented by a [Razor file (\*.cshtml)](xref:mvc/views/razor) or a [C# file (\*.cs)](/dotnet/csharp/getting-started/) compiled into a C# class assembly. Components are typical features found in web app client UIs, such as a page, dialog, or form, along with its client logic. Components are the fundamental building blocks of Blazor apps and can be nested, reused, and shared between projects.

## Use of Razor



## Inline vs code behind



## Event handling



## Data binding and validation



## Render child content



## Provide parameters



## Specify child content



## Routing


## JavaScript/TypeScript interop

To call JavaScript libraries or custom JavaScript/TypeScript code from .NET, the current approach is to register a named function in a JavaScript/TypeScript file:

```javascript
Blazor.registerFunction('doPrompt', message => {
  return prompt(message);
});
```

Wrap the named function for calls from .NET:

```csharp
public static bool DoPrompt(string message)
{
    return RegisteredFunction.Invoke<bool>("doPrompt", message);
}
```

This approach has the benefit of working with JavaScript build tools, such as [webpack](https://webpack.js.org/).

The Mono team is working on a library that exposes standard browser APIs to .NET.
