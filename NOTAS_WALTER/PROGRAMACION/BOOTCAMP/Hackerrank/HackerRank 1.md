
# Ejercicio 1:
****
## Problema
![[Pasted image 20260807133338.png]]

## Codigo 
```
import java.io.*;

import java.math.*;

import java.security.*;

import java.text.*;

import java.util.*;

import java.util.concurrent.*;

import java.util.regex.*;

  

public class Solution {

  
  
  

    private static final Scanner scanner = new Scanner(System.in);

  

    public static void main(String[] args) {

        int N = scanner.nextInt();

        scanner.skip("(\r\n|[\n\r\u2028\u2029\u0085])?");

        if ( N < 1 || N >100){

            return;

        }

        else {

            if ( N%2!=0){

            System.out.println("Weird");

        }

        else {

             if(N <5 && N>2 ){

                System.out.println("Not Weird");

            }

            else {

                if (N>=6 && N<=20){

                    System.out.println("Weird");

                }

                else {

                        System.out.println("Not Weird");

  

            }

        }

  

        }

        scanner.close();

    }

    }}
```


## Pantallazo de prueba
![[Pasted image 20260807133246.png]]




****
# Ejercicio 2


## Problema

![[Pasted image 20260807135308.png]]

## codigo
```
import java.util.Scanner;

  

public class Solution {

  

    public static void main(String[] args) {

        Scanner scan = new Scanner(System.in);

        int i = scan.nextInt();

        scan.nextLine();

        double d =scan.nextDouble();

        scan.nextLine();

        String s = scan.nextLine();

  

        // Write your code here

        System.out.println("String: " + s);

        System.out.println("Double: " + d);

        System.out.println("Int: " + i);

        scan.close();

    }

}
```



## Pantallazo de Prueba

![[Pasted image 20260807135412.png|749]]

****
# Ejercicio 3

## Problema

![[Pasted image 20260807141211.png]]

## Codigo 
```
import java.util.Scanner;

  

public class Solution {

  

    public static void main(String[] args) {

            Scanner sc=new Scanner(System.in);

            System.out.println("================================");

            for(int i=0;i<3;i++){

                String s1=sc.next();

                int x=sc.nextInt();

                //Complete this line

                System.out.printf("%-15s%03d%n", s1 ,x);

            }

            System.out.println("================================");

  

    }

}
```



## Pantallazo prueba

![[Pasted image 20260807141250.png]]