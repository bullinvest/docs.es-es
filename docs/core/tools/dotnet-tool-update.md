---
title: Comando dotnet tool update - CLI de .NET Core
description: El comando dotnet tool update actualiza la herramienta global de .NET Core en su equipo.
author: mairaw
ms.author: mairaw
ms.date: 05/29/2018
ms.openlocfilehash: 35a0bd0f85f0beed06d4250d8f195ce4fe4fcca4
ms.sourcegitcommit: bbf70abe6b46073148f78cbf0619de6092b5800c
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 06/04/2018
ms.locfileid: "34696694"
---
# <a name="dotnet-tool-update"></a><span data-ttu-id="8d8f7-103">dotnet tool update</span><span class="sxs-lookup"><span data-stu-id="8d8f7-103">dotnet tool update</span></span>

[!INCLUDE [topic-appliesto-net-core-21plus.md](../../../includes/topic-appliesto-net-core-21plus.md)]

## <a name="name"></a><span data-ttu-id="8d8f7-104">nombre</span><span class="sxs-lookup"><span data-stu-id="8d8f7-104">Name</span></span>

<span data-ttu-id="8d8f7-105">`dotnet tool update`: actualiza la [herramienta global de .NET Core](global-tools.md) especificada en el equipo.</span><span class="sxs-lookup"><span data-stu-id="8d8f7-105">`dotnet tool update` - Updates the specified [.NET Core Global Tool](global-tools.md) on your machine.</span></span>

## <a name="synopsis"></a><span data-ttu-id="8d8f7-106">Sinopsis</span><span class="sxs-lookup"><span data-stu-id="8d8f7-106">Synopsis</span></span>

```
dotnet tool update <PACKAGE_NAME> <-g|--global> [--configfile] [--framework] [-v|--verbosity]
dotnet tool update <PACKAGE_NAME> <--tool-path> [--configfile] [--framework] [-v|--verbosity]
dotnet tool update <-h|--help>
```

## <a name="description"></a><span data-ttu-id="8d8f7-107">Description</span><span class="sxs-lookup"><span data-stu-id="8d8f7-107">Description</span></span>

<span data-ttu-id="8d8f7-108">El comando `dotnet tool update` permite actualizar las herramientas globales de .NET Core en su equipo a la versión estable más reciente del paquete.</span><span class="sxs-lookup"><span data-stu-id="8d8f7-108">The `dotnet tool update` command provides a way for you to update .NET Core Global Tools on your machine to the latest stable version of the package.</span></span> <span data-ttu-id="8d8f7-109">El comando desinstala y vuelve a instalar una herramienta, actualizándola de facto.</span><span class="sxs-lookup"><span data-stu-id="8d8f7-109">The command uninstalls and reinstalls a tool, effectively updating it.</span></span> <span data-ttu-id="8d8f7-110">Para utilizar el comando, especifique que quiere actualizar una herramienta de una instalación en el ámbito de los usuarios con la opción `--global`, o bien especifique una ruta de acceso en la que instalar la herramienta usando para ello la opción `--tool-path`.</span><span class="sxs-lookup"><span data-stu-id="8d8f7-110">To use the command, you either have to specify that you want to update a tool from a user-wide installation using the `--global` option or specify a path to where the tool is installed using the `--tool-path` option.</span></span>

## <a name="arguments"></a><span data-ttu-id="8d8f7-111">Argumentos</span><span class="sxs-lookup"><span data-stu-id="8d8f7-111">Arguments</span></span>

`PACKAGE_NAME`

<span data-ttu-id="8d8f7-112">Nombre o identificador del paquete de NuGet que contiene la herramienta global de .NET Core que se quiere actualizar.</span><span class="sxs-lookup"><span data-stu-id="8d8f7-112">Name/ID of the NuGet package that contains the .NET Core Global Tool to update.</span></span> <span data-ttu-id="8d8f7-113">Para conocer el nombre el paquete, use el comando [dotnet tool list](dotnet-tool-list.md).</span><span class="sxs-lookup"><span data-stu-id="8d8f7-113">You can find the package name using the [dotnet tool list](dotnet-tool-list.md) command.</span></span>

## <a name="options"></a><span data-ttu-id="8d8f7-114">Opciones</span><span class="sxs-lookup"><span data-stu-id="8d8f7-114">Options</span></span>

`--add-source <SOURCE>`

<span data-ttu-id="8d8f7-115">Agrega un origen de paquete NuGet adicional que se usará durante la instalación.</span><span class="sxs-lookup"><span data-stu-id="8d8f7-115">Adds an additional NuGet package source to use during installation.</span></span>

`--configfile <FILE>`

<span data-ttu-id="8d8f7-116">El archivo de configuración de NuGet (*nuget.config*) que se usará.</span><span class="sxs-lookup"><span data-stu-id="8d8f7-116">The NuGet configuration (*nuget.config*) file to use.</span></span>

`--framework <FRAMEWORK>`

<span data-ttu-id="8d8f7-117">Especifica la [plataforma de destino](../../standard/frameworks.md) para la que se actualiza la herramienta.</span><span class="sxs-lookup"><span data-stu-id="8d8f7-117">Specifies the [target framework](../../standard/frameworks.md) to update the tool for.</span></span>

`-g|--global`

<span data-ttu-id="8d8f7-118">Especifica que la actualización es para una herramienta del ámbito de los usuarios.</span><span class="sxs-lookup"><span data-stu-id="8d8f7-118">Specifies that the update is for a user-wide tool.</span></span> <span data-ttu-id="8d8f7-119">No se puede combinar con la opción `--tool-path`.</span><span class="sxs-lookup"><span data-stu-id="8d8f7-119">Can't be combined with the `--tool-path` option.</span></span> <span data-ttu-id="8d8f7-120">Si no especifica esta opción, debe especificar la opción `--tool-path`.</span><span class="sxs-lookup"><span data-stu-id="8d8f7-120">If you don't specify this option, you must specify the `--tool-path` option.</span></span>

`-h|--help`

<span data-ttu-id="8d8f7-121">Imprime una corta ayuda para el comando.</span><span class="sxs-lookup"><span data-stu-id="8d8f7-121">Prints out a short help for the command.</span></span>

`--tool-path <PATH>`

<span data-ttu-id="8d8f7-122">Especifica la ubicación en la que está instalada la herramienta global.</span><span class="sxs-lookup"><span data-stu-id="8d8f7-122">Specifies the location where the Global Tool is installed.</span></span> <span data-ttu-id="8d8f7-123">PATH puede ser una ruta absoluta o relativa.</span><span class="sxs-lookup"><span data-stu-id="8d8f7-123">PATH can be absolute or relative.</span></span> <span data-ttu-id="8d8f7-124">No se puede combinar con la opción `--global`.</span><span class="sxs-lookup"><span data-stu-id="8d8f7-124">Can't be combined with the `--global` option.</span></span> <span data-ttu-id="8d8f7-125">Si no especifica esta opción, debe especificar la opción `--global`.</span><span class="sxs-lookup"><span data-stu-id="8d8f7-125">If you don't specify this option, you must specify the `--global` option.</span></span>

`-v|--verbosity <LEVEL>`

<span data-ttu-id="8d8f7-126">Establece el nivel de detalle del comando.</span><span class="sxs-lookup"><span data-stu-id="8d8f7-126">Sets the verbosity level of the command.</span></span> <span data-ttu-id="8d8f7-127">Los valores permitidos son `q[uiet]`, `m[inimal]`, `n[ormal]`, `d[etailed]` y `diag[nostic]`.</span><span class="sxs-lookup"><span data-stu-id="8d8f7-127">Allowed values are `q[uiet]`, `m[inimal]`, `n[ormal]`, `d[etailed]`, and `diag[nostic]`.</span></span>

## <a name="examples"></a><span data-ttu-id="8d8f7-128">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="8d8f7-128">Examples</span></span>

<span data-ttu-id="8d8f7-129">Actualiza la herramienta global [dotnetsay](https://www.nuget.org/packages/dotnetsay/):</span><span class="sxs-lookup"><span data-stu-id="8d8f7-129">Updates the [dotnetsay](https://www.nuget.org/packages/dotnetsay/) Global Tool:</span></span>

`dotnet tool update -g dotnetsay`

<span data-ttu-id="8d8f7-130">Actualiza la herramienta global [dotnetsay](https://www.nuget.org/packages/dotnetsay/) ubicada en una carpeta específica de Windows:</span><span class="sxs-lookup"><span data-stu-id="8d8f7-130">Updates the [dotnetsay](https://www.nuget.org/packages/dotnetsay/) Global Tool located on a specific Windows folder:</span></span>

`dotnet tool update dotnetsay --tool-path c:\global-tools`

<span data-ttu-id="8d8f7-131">Actualiza la herramienta global [dotnetsay](https://www.nuget.org/packages/dotnetsay/) ubicada en una carpeta específica de Linux/macOS:</span><span class="sxs-lookup"><span data-stu-id="8d8f7-131">Updates the [dotnetsay](https://www.nuget.org/packages/dotnetsay/) Global Tool located on a specific Linux/macOS folder:</span></span>

`dotnet tool update dotnetsay --tool-path ~/bin`

## <a name="see-also"></a><span data-ttu-id="8d8f7-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="8d8f7-132">See also</span></span>

[<span data-ttu-id="8d8f7-133">Herramientas globales de .NET Core</span><span class="sxs-lookup"><span data-stu-id="8d8f7-133">.NET Core Global Tools</span></span>](global-tools.md)