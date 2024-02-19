<!--
author:   Robert Kunze
email:    Mark.Jacob@iuz.tu-freiberg.de
version:  0.0.1
language: en

import: https://github.com/liascript/CodeRunner

dark:     true

mode: Presentation

-->

# Bubble Sorting in C#

![image alt](https://upload.wikimedia.org/wikipedia/commons/c/c8/Bubble-sort-example-300px.gif)

## whats that?

A sorting algorithm which is sorting numbers in our case.



## explanation of how it works:

![image alt](https://miro.medium.com/max/776/1*7QsZkfrRGhAu5yxxeDdzsA.png)
<br>
![image alt](https://upload.wikimedia.org/wikipedia/commons/c/c8/Bubble-sort-example-300px.gif)

### how we do it in code

```csharp        BubSort
using System;
using System.Text; 
public class Program
{
    static void bubbleSort(int []arr)
    {
        int n = arr.Length;
        bool sorted= false;
        while(!sorted)
        {
            sorted = true;
            for (int i = 0; i < n - 1; i++)
                if (arr[i] > arr[i+1])
                {
                    int temp = arr[i];
                    arr[i] = arr[i+1];
                    arr[i+1] = temp;
                    sorted = false;
                }
        }
        
    }
 
}
 
```


## raw code

```csharp        BubSort
using System;
using System.Text; 
public class Program
{
    static void bubbleSort(int []arr)
    {
        int n = arr.Length;
        bool sorted= false;
        while(!sorted)
        {
            sorted = true;
            for (int i = 0; i < n - 1; i++)
                if (arr[i] > arr[i+1])
                {
                    int temp = arr[i];
                    arr[i] = arr[i+1];
                    arr[i+1] = temp;
                    sorted = false;
                }
        }
        
    }
 
    static void printArray(int []arr)
    {
        int n = arr.Length;
        for (int i = 0; i < n; ++i)
            Console.Write(arr[i] + " ");
        Console.WriteLine();
    }
    
 
    public static void Main()
    {
        int []arr = {-22, 34, 0, -12, 22, 11, 90};
        bubbleSort(arr);
        Console.WriteLine("Sorted array");
        printArray(arr);
    }
}
 
```
@LIA.eval(`["main.cs"]`, `mono main.cs`, `mono main.exe`)

## Pros and cons

Pros: <br>
Simplicity and ease of implementation <br><br>
Cons: <br>
Horribly inefficient
![image alt](https://cdn.discordapp.com/attachments/550280788445495306/858959491819241472/bubble.png)

# Sources

https://whatis.techtarget.com/definition/sorting-algorithm

http://www.icodeguru.com/cpp/SortingAlgorithms/bubble.html#:~:text=Pros%3A%20Simplicity%20and%20ease%20of,Cons%3A%20Horribly%20inefficient.&text=The%20graph%20clearly%20shows%20the,be%20used%20for%20any%20reason.