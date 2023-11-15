# NewFunction2
/*
 * Click nbfs://nbhost/SystemFileSystem/Templates/Licenses/license-default.txt to change this license
 * Click nbfs://nbhost/SystemFileSystem/Templates/Project/Maven2/JavaApp/src/main/java/${packagePath}/${mainClassName}.java to edit this template
 */

package com.mycompany.mavenproject2;

import java.util.Scanner;

/**
 *
 * @author User
 */
public class Mavenproject2 {

   public static void main(String[] args) {
       
      String name;
        int age;
        int children;
        char gender;
        double salary;
        
        Scanner console=new Scanner(System.in);
        System.out.println("Enter name:");
        name=console.nextLine();
        System.out.println("Enter age:");
        age=console.nextInt();
        System.out.println("Enter gender:(F/M)");
        gender=console.next().charAt(0);
        System.out.println("Enter salary:");
        salary=console.nextDouble();
        System.out.println("Enter number of children");
        children=console.nextInt(); 
       
        printperson(name, age, gender, salary, children);
        
         String[]childrenNames=new String[children];
         int[]childrenAges=new int[children];
         
         if (children>0){
         for(int i = 0; i<children;i++){
                    System.out.println("Enter name:");
                    childrenNames[i]=console.nextLine();
                    System.out.println("Enter age:");
                    childrenAges[i]=console.nextInt();
                }
                
		printChildren(children,childrenNames,childrenAges);
}
    }
 
    static void printChildren(int childrenNumber, String childrenNames[],int childrenAge[]){
        for(int i = 0; i<childrenNumber;i++){
                    System.out.println(childrenNames[i]+", "+childrenAge[i]);
                }
    }
   
   public static void printperson(String empName, int empAge, char empGender, double empSalary, int empChildren){
        
        System.out.println("Name: "  + empName +  "\nAge: "+empAge+ "\nGender: " +empGender+ "\nSalary: "+empSalary+ "\nChildren: " +empChildren);
        if (empChildren>2){
            System.out.println("Salary is: " +(empSalary+(empSalary*0.20)));
        }else if(empChildren==0){
            System.out.println("Your salary is still the same");
        }
    }
}
