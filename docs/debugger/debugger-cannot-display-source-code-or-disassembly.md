---
title: "Debugger can't display source code or disassembly"
description: See the reasons for the message "Debugger cannot display source code or disassembly for the current location where execution has stopped". 

ms.date: "11/04/2016"
ms.topic: "conceptual"
dev_langs:
  - "CSharp"
  - "VB"
  - "FSharp"
  - "C++"
helpviewer_keywords:
  - "disassembly code, errors"
ms.assetid: 112d3ea3-fdd2-4bce-92b4-167a76258934
author: "mikejo5000"
ms.author: "mikejo"
manager: jmartens
ms.technology: vs-ide-debug
ms.workload:
  - "multiple"
---
# Debugger Cannot Display Source Code or Disassembly

 [!INCLUDE [Visual Studio](~/includes/applies-to-version/vs-windows-only.md)]
This error reads:

 The debugger cannot display source code or disassembly for the current location where execution has stopped.

 This error message can occur for a number of reasons:

- You may have hit a breakpoint in a location for which there is no source code, while debugging a language that doesn't support disassembly. Open the **Breakpoints** window, locate the breakpoint, and delete it.

- If you are debugging script, you may have hit a breakpoint while there were no threads in your program. Choose **Step** or **Continue** from the **Debug** menu to resume debugging.

- Security considerations may have prevented the debugger from reading stack, thread, register, and other context information from the program you are debugging. This is most likely to happen if you are debugging a Web application and don't have the right permission to access the virtual directory. Set security for the virtual directory to Anonymous and try again.

## See also
- [Debugging in Visual Studio](../debugger/index.yml)
- [First look at the debugger](../debugger/debugger-feature-tour.md)
- [Viewing Data in the Debugger](../debugger/viewing-data-in-the-debugger.md)