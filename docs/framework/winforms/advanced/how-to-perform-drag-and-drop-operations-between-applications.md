---
title: Procedimiento Realizar operaciones de arrastrar y colocar entre aplicaciones
ms.date: 03/30/2017
helpviewer_keywords:
- drag and drop [Windows Forms], between applications
ms.assetid: fa347436-2b12-4dd6-8507-59d7241f6a06
ms.openlocfilehash: 89b1b89c01ba80393e0965858d7767d5c9029003
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/23/2019
ms.locfileid: "54718443"
---
# <a name="how-to-perform-drag-and-drop-operations-between-applications"></a>Procedimiento Realizar operaciones de arrastrar y colocar entre aplicaciones
Realizar operaciones de arrastrar y colocar entre aplicaciones es similar a habilitar esta acción dentro de una aplicación, siempre que ambas aplicaciones implicadas se comporten según el "contrato" establecido entre las propiedades <xref:System.Windows.Forms.DragEventArgs.AllowedEffect%2A> y <xref:System.Windows.Forms.DragEventArgs.Effect%2A>.  
  
 En el siguiente procedimiento, usará una aplicación basada en Windows que cree y el procesador de textos WordPad que se incluye con el sistema operativo Windows para realizar operaciones de arrastrar y colocar entre aplicaciones. WordPad tiene un determinado conjunto de efectos permitidos para el texto que se va a arrastrar y colocar; la aplicación basada en Windows para la que escribirá el código trabajará con estos efectos para que las operaciones de arrastrar y colocar puedan completarse correctamente.  
  
### <a name="to-perform-a-drag-and-drop-procedure-between-applications"></a>Para realizar un procedimiento de arrastrar y colocar entre aplicaciones  
  
1.  Cree una nueva aplicación de Windows Forms.  
  
2.  Agregue un control <xref:System.Windows.Forms.TextBox> al formulario.  
  
3.  Configure el control <xref:System.Windows.Forms.TextBox> para recibir datos colocados.  
  
     Para obtener más información, vea [Tutorial: Realizar una operación de arrastrar y colocar en Windows Forms](../../../../docs/framework/winforms/advanced/walkthrough-performing-a-drag-and-drop-operation-in-windows-forms.md).  
  
4.  Ejecute la aplicación basada en Windows y, mientras la aplicación se está ejecutando, ejecute WordPad.  
  
     WordPad es un editor de texto instalado por Windows que permite operaciones de arrastrar y colocar. Es accesible presionando el **iniciar** button, seleccionar **ejecutar**y, a continuación, escriba `WordPad` en el cuadro de texto de la **ejecutar** cuadro de diálogo y haga clic en **Aceptar**.  
  
5.  Una vez abierto WordPad, escriba una cadena de texto en él.  
  
6.  Use el mouse para seleccionar el texto y, después, arrastre el texto seleccionado al control <xref:System.Windows.Forms.TextBox> de la aplicación basada en Windows.  
  
     Observe que, cuando el mouse se desplaza sobre el control <xref:System.Windows.Forms.TextBox> (y, por lo tanto, se genera el evento <xref:System.Windows.Forms.Control.DragEnter>), el cursor cambia y puede colocar el texto seleccionado en el control <xref:System.Windows.Forms.TextBox>.  
  
     También puede configurar su control <xref:System.Windows.Forms.TextBox> para poder arrastrar y colocar cadenas de texto en WordPad. Para obtener más información, vea [Tutorial: Realizar una operación de arrastrar y colocar en Windows Forms](../../../../docs/framework/winforms/advanced/walkthrough-performing-a-drag-and-drop-operation-in-windows-forms.md).  
  
## <a name="see-also"></a>Vea también
- [Cómo: Agregar datos al Portapapeles](../../../../docs/framework/winforms/advanced/how-to-add-data-to-the-clipboard.md)
- [Cómo: Recuperar datos del Portapapeles](../../../../docs/framework/winforms/advanced/how-to-retrieve-data-from-the-clipboard.md)
- [Compatibilidad con las operaciones de arrastrar y colocar y con el Portapapeles](../../../../docs/framework/winforms/advanced/drag-and-drop-operations-and-clipboard-support.md)
