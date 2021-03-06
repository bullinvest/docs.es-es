---
title: Procedimiento Mostrar un Control en la elija el cuadro de diálogo de elementos de cuadro de herramientas
ms.date: 03/30/2017
helpviewer_keywords:
- global assembly cache [Windows Forms], Choose Toolbox Items dialog box
- AssemblyFoldersEx [Windows Forms], Choose Toolbox Items dialog box
- controls [Windows Forms], display in Choose Toolbox Items dialog box
- assembly folder registration [Windows Forms], Choose Toolbox Items dialog box
- Choose Toolbox Items dialog box [Windows Forms], display control
ms.assetid: 01ef6eba-d044-40f0-951d-78eff7ebd9a9
ms.openlocfilehash: 3893859071b49c2ce0a01ca9d31fbee4474f21c9
ms.sourcegitcommit: 07c4368273b446555cb2c85397ea266b39d5fe50
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/21/2019
ms.locfileid: "56583161"
---
# <a name="how-to-display-a-control-in-the-choose-toolbox-items-dialog-box"></a>Filtrar Mostrar un Control en la elija el cuadro de diálogo de elementos de cuadro de herramientas
Desarrollar y distribuir controles, es posible que desee esos controles aparezca en el **elegir elementos del cuadro de herramientas** cuadro de diálogo que aparece cuando hace clic en el **cuadro de herramientas** y seleccione  **Elegir elementos**. Puede habilitar el control aparezca en este cuadro de diálogo mediante el procedimiento de registro AssemblyFoldersEx.  
  
### <a name="to-display-your-control-in-the-choose-toolbox-items-dialog-box"></a>Para mostrar el control en el cuadro de diálogo Elegir elementos del cuadro de herramientas  
  
-   Instale al ensamblado del control a la caché global de ensamblados. Para obtener más información, vea [Cómo: Instalar un ensamblado en la caché global de ensamblados](../../../../docs/framework/app-domains/how-to-install-an-assembly-into-the-gac.md)  
  
     O bien  
  
-   Registre el control y los ensamblados en tiempo de diseño asociados mediante el procedimiento de registro AssemblyFoldersEx. AssemblyFoldersEx es una ubicación del registro donde otros proveedores almacenan las rutas de acceso para cada versión de framework que admiten. Resolución de tiempo de diseño puede buscar en esta ubicación del registro para buscar los ensamblados de referencia. El script de registro puede especificar los controles que desee que aparezca en el cuadro de herramientas. Para obtener más información, consulte [implementar un Control personalizado y ensamblados en tiempo de diseño](https://docs.microsoft.com/previous-versions/visualstudio/visual-studio-2010/ee849818(v=vs.100)).  
  
## <a name="see-also"></a>Vea también
- [Elegir elementos del cuadro de herramientas (Cuadro de diálogo): Visual Studio](https://docs.microsoft.com/previous-versions/visualstudio/visual-studio-2010/dyca0t6t(v=vs.100))
- [Implementación de un Control personalizado y ensamblados en tiempo de diseño](https://docs.microsoft.com/previous-versions/visualstudio/visual-studio-2010/ee849818(v=vs.100))
- [Desarrollar controles de Windows Forms en tiempo de diseño](../../../../docs/framework/winforms/controls/developing-windows-forms-controls-at-design-time.md)
- [Cómo: Instalar un ensamblado en la caché global de ensamblados](../../../../docs/framework/app-domains/how-to-install-an-assembly-into-the-gac.md)
- [Tutorial: Rellenar automáticamente el cuadro de herramientas con componentes personalizados](../../../../docs/framework/winforms/controls/walkthrough-automatically-populating-the-toolbox-with-custom-components.md)
