---
title: 'Ramas y bucles: tutorial de introducción a C#'
description: En este tutorial sobre ramas y bucles, escribirá código de C# para explorar la sintaxis del lenguaje que admite ramas y bucles condicionales para ejecutar instrucciones de forma repetida.
ms.date: 10/31/2017
ms.custom: mvc
ms.openlocfilehash: 0997c0b4a8f450c0e5eadc9616457a1ab84e7d96
ms.sourcegitcommit: c93fd5139f9efcf6db514e3474301738a6d1d649
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/27/2018
ms.locfileid: "50186145"
---
# <a name="learn-conditional-logic-with-branch-and-loop-statements"></a><span data-ttu-id="dd8f7-103">Obtenga información sobre la lógica condicional con instrucciones de rama y bucle</span><span class="sxs-lookup"><span data-stu-id="dd8f7-103">Learn conditional logic with branch and loop statements</span></span>

<span data-ttu-id="dd8f7-104">En este tutorial se enseña a escribir código que analiza variables y cambia la ruta de acceso de ejecución en función de dichas variables.</span><span class="sxs-lookup"><span data-stu-id="dd8f7-104">This tutorial teaches you how to write code that examines variables and changes the execution path based on those variables.</span></span> <span data-ttu-id="dd8f7-105">Escriba código de C# y vea los resultados de la compilación y la ejecución.</span><span class="sxs-lookup"><span data-stu-id="dd8f7-105">You write C# code and see the results of compiling and running it.</span></span> <span data-ttu-id="dd8f7-106">El tutorial contiene una serie de lecciones en las que se analizan las construcciones de bifurcaciones y bucles en C#.</span><span class="sxs-lookup"><span data-stu-id="dd8f7-106">The tutorial contains a series of lessons that explore branching and looping constructs in C#.</span></span> <span data-ttu-id="dd8f7-107">En ellas se enseñan los aspectos básicos del lenguaje C#.</span><span class="sxs-lookup"><span data-stu-id="dd8f7-107">These lessons teach you the fundamentals of the C# language.</span></span>

<span data-ttu-id="dd8f7-108">En este tutorial se supone que cuenta con una máquina que puede usar para el desarrollo.</span><span class="sxs-lookup"><span data-stu-id="dd8f7-108">This tutorial expects you to have a machine you can use for development.</span></span> <span data-ttu-id="dd8f7-109">El tema de .NET [Iniciar en 10 minutos](https://www.microsoft.com/net/core) cuenta con instrucciones para configurar el entorno de desarrollo local en Mac, PC o Linux.</span><span class="sxs-lookup"><span data-stu-id="dd8f7-109">The .NET topic [Get Started in 10 minutes](https://www.microsoft.com/net/core) has instructions for setting up your local development environment on Mac, PC or Linux.</span></span> <span data-ttu-id="dd8f7-110">En [Become familiar with the development tools](local-environment.md) (Familiarizarse con las herramientas de desarrollo) puede obtener información general sobre los comandos que usará, donde hay vínculos que amplían la información.</span><span class="sxs-lookup"><span data-stu-id="dd8f7-110">A quick overview of the commands you'll use is in the [Become familiar with the development tools](local-environment.md) with links to more details.</span></span>

## <a name="make-decisions-using-the-if-statement"></a><span data-ttu-id="dd8f7-111">Toma de decisiones con la instrucción `if`.</span><span class="sxs-lookup"><span data-stu-id="dd8f7-111">Make decisions using the `if` statement</span></span>

<span data-ttu-id="dd8f7-112">Cree un directorio denominado **branches-tutorial**.</span><span class="sxs-lookup"><span data-stu-id="dd8f7-112">Create a directory named **branches-tutorial**.</span></span> <span data-ttu-id="dd8f7-113">Conviértalo en el directorio actual y ejecute `dotnet new console -n BranchesAndLoops -o .`.</span><span class="sxs-lookup"><span data-stu-id="dd8f7-113">Make that the current directory and run `dotnet new console -n BranchesAndLoops -o .`.</span></span> <span data-ttu-id="dd8f7-114">Este comando crea una nueva aplicación de consola de .NET Core en el directorio actual.</span><span class="sxs-lookup"><span data-stu-id="dd8f7-114">This command creates a new .NET Core console application in the current directory.</span></span>

<span data-ttu-id="dd8f7-115">Abra **Program.cs** en su editor favorito y reemplace la línea `Console.Writeline("Hello World!");` por el código siguiente:</span><span class="sxs-lookup"><span data-stu-id="dd8f7-115">Open **Program.cs** in your favorite editor, and replace the line `Console.Writeline("Hello World!");` with the following code:</span></span>

```csharp
int a = 5;
int b = 6;
if (a + b > 10)
    Console.WriteLine("The answer is greater than 10.");
```

<span data-ttu-id="dd8f7-116">Pruebe este código escribiendo `dotnet run` en la ventana de la consola.</span><span class="sxs-lookup"><span data-stu-id="dd8f7-116">Try this code by typing `dotnet run` in your console window.</span></span> <span data-ttu-id="dd8f7-117">Debería ver el mensaje "The answer is greater than 10" (La respuesta es mayor que 10)</span><span class="sxs-lookup"><span data-stu-id="dd8f7-117">You should see the message "The answer is greater than 10."</span></span> <span data-ttu-id="dd8f7-118">impreso en la consola.</span><span class="sxs-lookup"><span data-stu-id="dd8f7-118">printed to your console.</span></span>

<span data-ttu-id="dd8f7-119">Modifique la declaración de `b` para que el resultado de la suma sea menor que diez:</span><span class="sxs-lookup"><span data-stu-id="dd8f7-119">Modify the declaration of `b` so that the sum is less than 10:</span></span> 

```csharp
int b = 3;
```

<span data-ttu-id="dd8f7-120">Escriba `dotnet run` de nuevo.</span><span class="sxs-lookup"><span data-stu-id="dd8f7-120">Type `dotnet run` again.</span></span> <span data-ttu-id="dd8f7-121">Como la respuesta es menor que diez, no se imprime nada.</span><span class="sxs-lookup"><span data-stu-id="dd8f7-121">Because the answer is less than 10, nothing is printed.</span></span> <span data-ttu-id="dd8f7-122">La **condición** que está probando es false.</span><span class="sxs-lookup"><span data-stu-id="dd8f7-122">The **condition** you're testing is false.</span></span> <span data-ttu-id="dd8f7-123">No tiene ningún código para ejecutar porque solo ha escrito una de las bifurcaciones posibles para una instrucción `if`: la bifurcación true.</span><span class="sxs-lookup"><span data-stu-id="dd8f7-123">You don't have any code to execute because you've only written one of the possible branches for an `if` statement: the true branch.</span></span>

> [!TIP]
> <span data-ttu-id="dd8f7-124">Cuando explore C# o cualquier otro lenguaje de programación, cometerá errores al escribir código.</span><span class="sxs-lookup"><span data-stu-id="dd8f7-124">As you explore C# (or any programming language), you'll make mistakes when you write code.</span></span> <span data-ttu-id="dd8f7-125">El compilador buscará dichos errores y los notificará.</span><span class="sxs-lookup"><span data-stu-id="dd8f7-125">The compiler will find and report the errors.</span></span> <span data-ttu-id="dd8f7-126">Fíjese en la salida de error y en el código que generó el error.</span><span class="sxs-lookup"><span data-stu-id="dd8f7-126">Look closely at the error output and the code that generated the error.</span></span> <span data-ttu-id="dd8f7-127">El error del compilador normalmente puede ayudarle a encontrar el problema.</span><span class="sxs-lookup"><span data-stu-id="dd8f7-127">The compiler error can usually help you find the problem.</span></span>

<span data-ttu-id="dd8f7-128">En este primer ejemplo se muestran la potencia de `if` y los tipos booleanos.</span><span class="sxs-lookup"><span data-stu-id="dd8f7-128">This first sample shows the power of `if` and Boolean types.</span></span> <span data-ttu-id="dd8f7-129">Un *booleano* es una variable que puede tener uno de estos dos valores: `true` o `false`.</span><span class="sxs-lookup"><span data-stu-id="dd8f7-129">A *Boolean* is a variable that can have one of two values: `true` or `false`.</span></span> <span data-ttu-id="dd8f7-130">C# define un tipo especial `bool` para las variables booleanas.</span><span class="sxs-lookup"><span data-stu-id="dd8f7-130">C# defines a special type, `bool` for Boolean variables.</span></span> <span data-ttu-id="dd8f7-131">La instrucción `if` comprueba el valor de `bool`.</span><span class="sxs-lookup"><span data-stu-id="dd8f7-131">The `if` statement checks the value of a `bool`.</span></span> <span data-ttu-id="dd8f7-132">Cuando el valor es `true`, se ejecuta la instrucción que sigue a `if`.</span><span class="sxs-lookup"><span data-stu-id="dd8f7-132">When the value is `true`, the statement following the `if` executes.</span></span> <span data-ttu-id="dd8f7-133">De lo contrario, se omite.</span><span class="sxs-lookup"><span data-stu-id="dd8f7-133">Otherwise, it is skipped.</span></span>

<span data-ttu-id="dd8f7-134">Este proceso de comprobación de condiciones y ejecución de instrucciones en función de esas condiciones es muy eficaz.</span><span class="sxs-lookup"><span data-stu-id="dd8f7-134">This process of checking conditions and executing statements based on those conditions is very powerful.</span></span>

## <a name="make-if-and-else-work-together"></a><span data-ttu-id="dd8f7-135">Operaciones conjuntas con if y else</span><span class="sxs-lookup"><span data-stu-id="dd8f7-135">Make if and else work together</span></span>

<span data-ttu-id="dd8f7-136">Para ejecutar un código distinto en las bifurcaciones true y false, cree una bifurcación `else` para que se ejecute cuando la condición sea false.</span><span class="sxs-lookup"><span data-stu-id="dd8f7-136">To execute different code in both the true and false branches, you create an `else` branch that executes when the condition is false.</span></span> <span data-ttu-id="dd8f7-137">Pruebe esto.</span><span class="sxs-lookup"><span data-stu-id="dd8f7-137">Try this.</span></span> <span data-ttu-id="dd8f7-138">Agregue las dos últimas líneas del código siguiente a su método `Main` (ya debe tener los cuatro primeros):</span><span class="sxs-lookup"><span data-stu-id="dd8f7-138">Add the last two lines in the code below to your `Main` method (you should already have the first four):</span></span>

```csharp
int a = 5;
int b = 3;
if (a + b > 10)
    Console.WriteLine("The answer is greater than 10");
else
    Console.WriteLine("The answer is not greater than 10");
```

<span data-ttu-id="dd8f7-139">La instrucción que sigue a la palabra clave `else` se ejecuta solo si la condición de prueba es `false`.</span><span class="sxs-lookup"><span data-stu-id="dd8f7-139">The statement following the `else` keyword executes only when the condition being tested is `false`.</span></span> <span data-ttu-id="dd8f7-140">La combinación de `if` y `else` con condiciones booleanas ofrece toda la eficacia necesaria para administrar una condición `true` y `false` simultáneamente.</span><span class="sxs-lookup"><span data-stu-id="dd8f7-140">Combining `if` and `else` with Boolean conditions provides all the power you need to handle both a `true` and a `false` condition.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="dd8f7-141">La sangría debajo de las instrucciones `if` y `else` se utiliza para los lectores humanos.</span><span class="sxs-lookup"><span data-stu-id="dd8f7-141">The indentation under the `if` and `else` statements is for human readers.</span></span>
> <span data-ttu-id="dd8f7-142">El lenguaje C# no considera significativos los espacios en blanco ni las sangrías.</span><span class="sxs-lookup"><span data-stu-id="dd8f7-142">The C# language doesn't treat indentation or white space as significant.</span></span> <span data-ttu-id="dd8f7-143">La instrucción que sigue a la palabra clave `if` o `else` se ejecutará en función de la condición.</span><span class="sxs-lookup"><span data-stu-id="dd8f7-143">The statement following the `if` or `else` keyword will be executed based on the condition.</span></span> <span data-ttu-id="dd8f7-144">Todos los ejemplos de este tutorial siguen una práctica común para aplicar sangría a las líneas en función del flujo de control de las instrucciones.</span><span class="sxs-lookup"><span data-stu-id="dd8f7-144">All the samples in this tutorial follow a common practice to indent lines based on the control flow of statements.</span></span>

<span data-ttu-id="dd8f7-145">Dado que la sangría no es significativa, debe usar `{` y `}` para indicar si desea que más de una instrucción forme parte del bloque que se ejecuta de forma condicional.</span><span class="sxs-lookup"><span data-stu-id="dd8f7-145">Because indentation is not significant, you need to use `{` and `}` to indicate when you want more than one statement to be part of the block that executes conditionally.</span></span> <span data-ttu-id="dd8f7-146">Los programadores de C# suelen usar esas llaves en todas las cláusulas `if` y `else`.</span><span class="sxs-lookup"><span data-stu-id="dd8f7-146">C# programmers typically use those braces on all `if` and `else` clauses.</span></span> <span data-ttu-id="dd8f7-147">El siguiente ejemplo es igual al que acaba de crear.</span><span class="sxs-lookup"><span data-stu-id="dd8f7-147">The following example is the same as the one you just created.</span></span> <span data-ttu-id="dd8f7-148">Modifique el código anterior para que coincida con el código siguiente:</span><span class="sxs-lookup"><span data-stu-id="dd8f7-148">Modify your code above to match the following code:</span></span>

```csharp
int a = 5;
int b = 3;
if (a + b > 10)
{
    Console.WriteLine("The answer is greater than 10");
}
else
{
    Console.WriteLine("The answer is not greater than 10");
}
```

> [!TIP]
> <span data-ttu-id="dd8f7-149">En el resto de este tutorial, todos los ejemplos de código incluyen las llaves, según las prácticas aceptadas.</span><span class="sxs-lookup"><span data-stu-id="dd8f7-149">Through the rest of this tutorial, the code samples all include the braces, following accepted practices.</span></span>

<span data-ttu-id="dd8f7-150">Puede probar condiciones más complicadas.</span><span class="sxs-lookup"><span data-stu-id="dd8f7-150">You can test more complicated conditions.</span></span> <span data-ttu-id="dd8f7-151">Agregue el código siguiente a su método `Main` después del código que ha escrito hasta ahora:</span><span class="sxs-lookup"><span data-stu-id="dd8f7-151">Add the following code in your `Main` method after the code you've written so far:</span></span>

```csharp
int c = 4;
if ((a + b + c > 10) && (a > b))
{
    Console.WriteLine("The answer is greater than 10");
    Console.WriteLine("And the first number is greater than the second");
}
else
{
    Console.WriteLine("The answer is not greater than 10");
    Console.WriteLine("Or the first number is not greater than the second");
}
```

<span data-ttu-id="dd8f7-152">`&&` representa "y".</span><span class="sxs-lookup"><span data-stu-id="dd8f7-152">The `&&` represents "and".</span></span> <span data-ttu-id="dd8f7-153">Significa que ambas condiciones deben cumplirse para ejecutar la instrucción en la bifurcación true.</span><span class="sxs-lookup"><span data-stu-id="dd8f7-153">It means both conditions must be true to execute the statement in the true branch.</span></span>  <span data-ttu-id="dd8f7-154">En estos ejemplos también se muestra que puede tener varias instrucciones en cada bifurcación condicional, siempre que las encierre entre `{` y `}`.</span><span class="sxs-lookup"><span data-stu-id="dd8f7-154">These examples also show that you can have multiple statements in each conditional branch, provided you enclose them in `{` and `}`.</span></span>

<span data-ttu-id="dd8f7-155">También puede usar `||` para representar "o".</span><span class="sxs-lookup"><span data-stu-id="dd8f7-155">You can also use  `||` to represent "or".</span></span> <span data-ttu-id="dd8f7-156">Agregue el código siguiente antes del que ha escrito hasta ahora:</span><span class="sxs-lookup"><span data-stu-id="dd8f7-156">Add the following code after what you've written so far:</span></span>

```csharp
if ((a + b + c > 10) || (a > b))
{
    Console.WriteLine("The answer is greater than 10");
    Console.WriteLine("Or the first number is greater than the second");
}
else
{
    Console.WriteLine("The answer is not greater than 10");
    Console.WriteLine("And the first number is not greater than the second");
}
```

<span data-ttu-id="dd8f7-157">Ha terminado el primer paso.</span><span class="sxs-lookup"><span data-stu-id="dd8f7-157">You've finished the first step.</span></span> <span data-ttu-id="dd8f7-158">Antes comenzar con la siguiente sección, se va a mover el código actual a un método independiente.</span><span class="sxs-lookup"><span data-stu-id="dd8f7-158">Before you start the next section, let's move the current code into a separate method.</span></span> <span data-ttu-id="dd8f7-159">Con este paso, resulta más fácil empezar con un nuevo ejemplo.</span><span class="sxs-lookup"><span data-stu-id="dd8f7-159">That makes it easier to start working with a new example.</span></span> <span data-ttu-id="dd8f7-160">Cambie el nombre del método `Main` por `ExploreIf` y escriba un método `Main` nuevo que llame a `ExploreIf`.</span><span class="sxs-lookup"><span data-stu-id="dd8f7-160">Rename your `Main` method to `ExploreIf` and write a new `Main` method that calls `ExploreIf`.</span></span> <span data-ttu-id="dd8f7-161">Cuando termine, el código debe tener un aspecto similar al siguiente:</span><span class="sxs-lookup"><span data-stu-id="dd8f7-161">When you have finished, your code should look like this:</span></span>

```csharp
using System;

namespace BranchesAndLoops
{
    class Program
    {
        static void ExploreIf()
        {
            int a = 5;
            int b = 3;
            if (a + b > 10)
            {
                Console.WriteLine("The answer is greater than 10");
            }
            else
            {
                Console.WriteLine("The answer is not greater than 10");
            }

            if ((a + b + c > 10) && (a > b))
            {
                Console.WriteLine("The answer is greater than 10");
                Console.WriteLine("And the first number is greater than the second");
            }
            else
            {
                Console.WriteLine("The answer is not greater than 10");
                Console.WriteLine("Or the first number is not greater than the second");
            }

            if ((a + b + c > 10) || (a > b))
            {
                Console.WriteLine("The answer is greater than 10");
                Console.WriteLine("Or the first number is greater than the second");
            }
            else
            {
                Console.WriteLine("The answer is not greater than 10");
                Console.WriteLine("And the first number is not greater than the second");
            }            
        }

        static void Main(string[] args)
        {
            ExploreIf();
        }
    }
}
```

<span data-ttu-id="dd8f7-162">Convierta en comentario la llamada a `ExploreIf()`.</span><span class="sxs-lookup"><span data-stu-id="dd8f7-162">Comment out the call to `ExploreIf()`.</span></span> <span data-ttu-id="dd8f7-163">De este modo la salida estará menos saturada a medida que trabaje en esta sección:</span><span class="sxs-lookup"><span data-stu-id="dd8f7-163">It will make the output less cluttered as you work in this section:</span></span>

```csharp
//ExploreIf();
```

<span data-ttu-id="dd8f7-164">El `//` inicia un **comentario** en C#.</span><span class="sxs-lookup"><span data-stu-id="dd8f7-164">The `//` starts a **comment** in C#.</span></span> <span data-ttu-id="dd8f7-165">Los comentarios son cualquier texto que desea mantener en el código fuente pero que no se ejecuta como código.</span><span class="sxs-lookup"><span data-stu-id="dd8f7-165">Comments are any text you want to keep in your source code but not execute as code.</span></span> <span data-ttu-id="dd8f7-166">El compilador no genera ningún código ejecutable a partir de comentarios.</span><span class="sxs-lookup"><span data-stu-id="dd8f7-166">The compiler does not generate any executable code from comments.</span></span>

## <a name="use-loops-to-repeat-operations"></a><span data-ttu-id="dd8f7-167">Uso de bucles para repetir las operaciones</span><span class="sxs-lookup"><span data-stu-id="dd8f7-167">Use loops to repeat operations</span></span>

<span data-ttu-id="dd8f7-168">En esta sección se usan **bucles** para repetir las instrucciones.</span><span class="sxs-lookup"><span data-stu-id="dd8f7-168">In this section you use **loops** to repeat statements.</span></span> <span data-ttu-id="dd8f7-169">Pruebe este código en su método `Main`:</span><span class="sxs-lookup"><span data-stu-id="dd8f7-169">Try this code in your `Main` method:</span></span>

```csharp
int counter = 0;
while (counter < 10)
{
    Console.WriteLine($"Hello World! The counter is {counter}");
    counter++;
}
```

<span data-ttu-id="dd8f7-170">La instrucción `while` comprueba una condición y ejecuta la instrucción o el bloque de instrucciones que aparece después de `while`.</span><span class="sxs-lookup"><span data-stu-id="dd8f7-170">The `while` statement checks a condition and executes the statement or statement block following the `while`.</span></span> <span data-ttu-id="dd8f7-171">La comprobación de la condición y la ejecución de dichas instrucciones se repetirán hasta que la condición sea false.</span><span class="sxs-lookup"><span data-stu-id="dd8f7-171">It repeatedly checks the condition and executing those statements until the condition is false.</span></span>

<span data-ttu-id="dd8f7-172">En este ejemplo aparece otro operador nuevo.</span><span class="sxs-lookup"><span data-stu-id="dd8f7-172">There's one other new operator in this example.</span></span> <span data-ttu-id="dd8f7-173">El código `++` que aparece después de la variable `counter` es el operador de **incremento**.</span><span class="sxs-lookup"><span data-stu-id="dd8f7-173">The `++` after the `counter` variable is the **increment** operator.</span></span> <span data-ttu-id="dd8f7-174">Suma un valor de uno al valor de `counter` y almacena dicho valor en la variable de `counter`.</span><span class="sxs-lookup"><span data-stu-id="dd8f7-174">It adds 1 to the value of `counter` and stores that value in the `counter` variable.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="dd8f7-175">Asegúrese de que la condición del bucle `while` cambia a false mientras ejecuta el código.</span><span class="sxs-lookup"><span data-stu-id="dd8f7-175">Make sure that the `while` loop condition changes to false as you execute the code.</span></span> <span data-ttu-id="dd8f7-176">En caso contrario, se crea un **bucle infinito** donde nunca finaliza el programa.</span><span class="sxs-lookup"><span data-stu-id="dd8f7-176">Otherwise, you create an **infinite loop** where your program never ends.</span></span> <span data-ttu-id="dd8f7-177">Esto no está demostrado en este ejemplo, ya que tendrá que forzar al programa a cerrar mediante **CTRL-C** u otros medios.</span><span class="sxs-lookup"><span data-stu-id="dd8f7-177">That is not demonstrated in this sample, because you have to force your program to quit using **CTRL-C** or other means.</span></span>

<span data-ttu-id="dd8f7-178">El bucle `while` prueba la condición antes de ejecutar el código que sigue a `while`.</span><span class="sxs-lookup"><span data-stu-id="dd8f7-178">The `while` loop tests the condition before executing the code following the `while`.</span></span> <span data-ttu-id="dd8f7-179">El bucle `do` ... `while` primero ejecuta el código y después comprueba la condición.</span><span class="sxs-lookup"><span data-stu-id="dd8f7-179">The `do` ... `while` loop executes the code first, and then checks the condition.</span></span> <span data-ttu-id="dd8f7-180">Lo que ocurre con el bucle se muestra en el ejemplo de código siguiente:</span><span class="sxs-lookup"><span data-stu-id="dd8f7-180">The do while loop is shown in the following code:</span></span>

```csharp
counter = 0;
do
{
    Console.WriteLine($"Hello World! The counter is {counter}");
    counter++;
} while (counter < 10);
```

<span data-ttu-id="dd8f7-181">Este bucle `do` y el bucle `while` anterior generan el mismo resultado.</span><span class="sxs-lookup"><span data-stu-id="dd8f7-181">This `do` loop and the earlier `while` loop produce the same output.</span></span>

## <a name="work-with-the-for-loop"></a><span data-ttu-id="dd8f7-182">Operaciones con el bucle for</span><span class="sxs-lookup"><span data-stu-id="dd8f7-182">Work with the for loop</span></span>

<span data-ttu-id="dd8f7-183">El bucle **for** se utiliza con frecuencia en C#.</span><span class="sxs-lookup"><span data-stu-id="dd8f7-183">The **for** loop is commonly used in C#.</span></span> <span data-ttu-id="dd8f7-184">Pruebe este código en su método Main():</span><span class="sxs-lookup"><span data-stu-id="dd8f7-184">Try this code in your Main() method:</span></span>

```csharp
for(int index = 0; index < 10; index++)
{
    Console.WriteLine($"Hello World! The index is {index}");
} 
```

<span data-ttu-id="dd8f7-185">Funciona de la misma forma que los bucles `while` y `do` que ya ha usado.</span><span class="sxs-lookup"><span data-stu-id="dd8f7-185">This does the same work as the `while` loop and the `do` loop you've already used.</span></span> <span data-ttu-id="dd8f7-186">La instrucción `for` consta de tres partes que controlan su funcionamiento.</span><span class="sxs-lookup"><span data-stu-id="dd8f7-186">The `for` statement has three parts that control how it works.</span></span>

<span data-ttu-id="dd8f7-187">La primera parte es el **inicializador de for**: `for index = 0;` declara que `index` es la variable de bucle y establece su valor inicial en `0`.</span><span class="sxs-lookup"><span data-stu-id="dd8f7-187">The first part is the **for initializer**: `for index = 0;` declares that `index` is the loop variable, and sets its initial value to `0`.</span></span>

<span data-ttu-id="dd8f7-188">La parte central es la **condición de for**: `index < 10` declara que este bucle `for` debe continuar ejecutándose mientras que el valor del contador sea menor que diez.</span><span class="sxs-lookup"><span data-stu-id="dd8f7-188">The middle part is the **for condition**: `index < 10` declares that this `for` loop continues to execute as long as the value of counter is less than 10.</span></span>

<span data-ttu-id="dd8f7-189">La última parte es el **iterador de for**: `index++` especifica cómo modificar la variable de bucle después de ejecutar el bloque que sigue a la instrucción `for`.</span><span class="sxs-lookup"><span data-stu-id="dd8f7-189">The final part is the **for iterator**: `index++` specifies how to modify the loop variable after executing the block following the `for` statement.</span></span> <span data-ttu-id="dd8f7-190">En este caso, especifica que `index` debe incrementarse en uno cada vez que el bloque se ejecuta.</span><span class="sxs-lookup"><span data-stu-id="dd8f7-190">Here, it specifies that `index` should be incremented by 1 each time the block executes.</span></span>

<span data-ttu-id="dd8f7-191">Experimente con estas partes por su cuenta.</span><span class="sxs-lookup"><span data-stu-id="dd8f7-191">Experiment with these yourself.</span></span> <span data-ttu-id="dd8f7-192">Pruebe todos los pasos siguientes:</span><span class="sxs-lookup"><span data-stu-id="dd8f7-192">Try each of the following:</span></span>

- <span data-ttu-id="dd8f7-193">Cambie el inicializador para que se inicie en un valor distinto.</span><span class="sxs-lookup"><span data-stu-id="dd8f7-193">Change the initializer to start at a different value.</span></span>
- <span data-ttu-id="dd8f7-194">Cambie la condición para que se detenga en un valor diferente.</span><span class="sxs-lookup"><span data-stu-id="dd8f7-194">Change the condition to stop at a different value.</span></span>

<span data-ttu-id="dd8f7-195">Cuando haya terminado, escriba algo de código para practicar con lo que ha aprendido.</span><span class="sxs-lookup"><span data-stu-id="dd8f7-195">When you're done, let's move on to write some code yourself to use what you've learned.</span></span>

## <a name="combine-branches-and-loops"></a><span data-ttu-id="dd8f7-196">Combinación de ramas y bucles</span><span class="sxs-lookup"><span data-stu-id="dd8f7-196">Combine branches and loops</span></span>

<span data-ttu-id="dd8f7-197">Ahora que ya ha obtenido la información sobre el bucle `if` y las construcciones de bucles con el lenguaje C#, trate de escribir código de C# para obtener la suma de todos los enteros de uno a veinte que se puedan dividir entre tres.</span><span class="sxs-lookup"><span data-stu-id="dd8f7-197">Now that you've seen the `if` statement and the looping constructs in the C# language, see if you can write C# code to find the sum of all integers 1 through 20 that are divisible by 3.</span></span>  <span data-ttu-id="dd8f7-198">Tenga en cuenta las siguientes sugerencias:</span><span class="sxs-lookup"><span data-stu-id="dd8f7-198">Here are a few hints:</span></span>

- <span data-ttu-id="dd8f7-199">El operador `%` proporciona el resto de una operación de división.</span><span class="sxs-lookup"><span data-stu-id="dd8f7-199">The `%` operator gives you the remainder of a division operation.</span></span>
- <span data-ttu-id="dd8f7-200">La instrucción `if` genera la condición para saber si un número debe formar parte de la suma.</span><span class="sxs-lookup"><span data-stu-id="dd8f7-200">The `if` statement gives you the condition to see if a number should be part of the sum.</span></span>
- <span data-ttu-id="dd8f7-201">El bucle `for` puede facilitar la repetición de una serie de pasos para todos los números comprendidos entre el uno y el veinte.</span><span class="sxs-lookup"><span data-stu-id="dd8f7-201">The `for` loop can help you repeat a series of steps for all the numbers 1 through 20.</span></span>

<span data-ttu-id="dd8f7-202">Pruébelo usted mismo.</span><span class="sxs-lookup"><span data-stu-id="dd8f7-202">Try it yourself.</span></span> <span data-ttu-id="dd8f7-203">Después, revise cómo lo ha hecho.</span><span class="sxs-lookup"><span data-stu-id="dd8f7-203">Then check how you did.</span></span> <span data-ttu-id="dd8f7-204">Debe obtener 63 como respuesta.</span><span class="sxs-lookup"><span data-stu-id="dd8f7-204">You should get 63 for an answer.</span></span> <span data-ttu-id="dd8f7-205">Puede ver una respuesta posible mediante la [visualización del código completado en GitHub](https://github.com/dotnet/samples/tree/master/csharp/branches-quickstart/Program.cs#L46-L54).</span><span class="sxs-lookup"><span data-stu-id="dd8f7-205">You can see one possible answer by [viewing the completed code on GitHub](https://github.com/dotnet/samples/tree/master/csharp/branches-quickstart/Program.cs#L46-L54).</span></span>

<span data-ttu-id="dd8f7-206">Ha completado el tutorial "Bifurcaciones y bucles".</span><span class="sxs-lookup"><span data-stu-id="dd8f7-206">You've completed the "branches and loops" tutorial.</span></span>

<span data-ttu-id="dd8f7-207">Puede continuar con el tutorial de [interpolación de cadenas](interpolated-strings-local.md) en su propio entorno de desarrollo.</span><span class="sxs-lookup"><span data-stu-id="dd8f7-207">You can continue with the [String interpolation](interpolated-strings-local.md) tutorial in your own development environment.</span></span>

<span data-ttu-id="dd8f7-208">Puede obtener más información sobre estos conceptos en los temas siguientes:</span><span class="sxs-lookup"><span data-stu-id="dd8f7-208">You can learn more about these concepts in these topics:</span></span>

[<span data-ttu-id="dd8f7-209">Instrucciones If y else</span><span class="sxs-lookup"><span data-stu-id="dd8f7-209">If and else statement</span></span>](../../language-reference/keywords/if-else.md)  
[<span data-ttu-id="dd8f7-210">Instrucción while</span><span class="sxs-lookup"><span data-stu-id="dd8f7-210">While statement</span></span>](../../language-reference/keywords/while.md)  
[<span data-ttu-id="dd8f7-211">Instrucción do</span><span class="sxs-lookup"><span data-stu-id="dd8f7-211">Do statement</span></span>](../../language-reference/keywords/do.md)  
[<span data-ttu-id="dd8f7-212">Instrucción for</span><span class="sxs-lookup"><span data-stu-id="dd8f7-212">For statement</span></span>](../../language-reference/keywords/for.md)  