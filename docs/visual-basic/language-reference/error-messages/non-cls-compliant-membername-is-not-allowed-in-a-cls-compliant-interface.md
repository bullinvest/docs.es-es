---
title: <membername> no compatible con CLS no se permite en una interfaz compatible con CLS
ms.date: 07/20/2015
f1_keywords:
- bc40033
- vbc40033
helpviewer_keywords:
- BC40033
ms.assetid: 060c4b08-798e-40f1-94cf-c05c524f1b8a
ms.openlocfilehash: aeacc49faad6198a9341a1ec7d010f1cd173912d
ms.sourcegitcommit: 14355b4b2fe5bcf874cac96d0a9e6376b567e4c7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/30/2019
ms.locfileid: "55288982"
---
# <a name="non-cls-compliant-membername-is-not-allowed-in-a-cls-compliant-interface"></a>No compatible con CLS \<membername > no se permite en una interfaz conforme a CLS
Una propiedad, procedimiento o evento en una interfaz se marca como `<CLSCompliant(True)>` cuando la propia interfaz está marcada como `<CLSCompliant(False)>` o no está marcada.  
  
 Para una interfaz sea compatible con la [independencia del lenguaje y componentes independientes del lenguaje](../../../standard/language-independence-and-language-independent-components.md) (CLS), deben ser compatible con todos sus miembros.  
  
 Al aplicar <xref:System.CLSCompliantAttribute> a un elemento de programación, establezca el parámetro `isCompliant` del atributo en `True` o `False` para indicar conformidad o disconformidad. No hay ningún valor predeterminado para este parámetro, por lo que debe proporcionar uno.  
  
 Si no se aplica <xref:System.CLSCompliantAttribute> a un elemento, se considera que no es conforme.  
  
 De forma predeterminada, este mensaje es una advertencia. Para obtener más información sobre cómo ocultar las advertencias o cómo tratarlas como errores, vea [Configuring Warnings in Visual Basic](/visualstudio/ide/configuring-warnings-in-visual-basic).  
  
 **Identificador de error:** BC40033  
  
## <a name="to-correct-this-error"></a>Para corregir este error  
  
-   Si requiere conformidad con CLS y tiene control sobre el código fuente de interfaz, marque la interfaz como `<CLSCompliant(True)>` si todos sus miembros son conformes.  
  
-   Si requiere conformidad con CLS y no tiene control sobre el código fuente de interfaz, o si no cumple las condiciones ser compatible, defina a este miembro dentro de una interfaz diferente.  
  
-   Si necesita que este miembro permanezca dentro de su interfaz actual, quite el <xref:System.CLSCompliantAttribute> de su definición o márquelo como `<CLSCompliant(False)>`.  
  
## <a name="see-also"></a>Vea también
- [Interface (instrucción)](../../../visual-basic/language-reference/statements/interface-statement.md)

