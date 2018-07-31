# Hello-World
This is my 1st Repository

Hello there i like AIs and i want to become a Data Scintist.
one of my code in java

import java.util.*;
class Primepalin
{
    void accept()
    {
        Scanner sc=new Scanner(System.in);
        System.out.println("Enter a no.=");
        int n=sc.nextInt();
        display(n);
    }
    void display(int n)
    {
        int pr=Check_Prime(n);
        boolean pa=Check_Palindrome(n);
        if(pr == 1 && pa == true)
        System.out.println("The no is primepalin no.");
        else
        System.out.println("The no. is not a Primepalin no,");
    }
    int Check_Prime(int n)
    {
        int c=0;
        for(int i=2;i<=n/2;i++)
        {
            if(n%i==0)
            {
            c++;
            break;
        }
       }
        if(c==0)
        return 1;
        else
        return 0;
        
    }
    boolean Check_Palindrome(int n)
    {
        int m=n,r=0;
        while(m!=0)
        {
            r=r*10+(m%10);
            m/=10;
        }
        if(n==r)
        return true;
        else
        return false;
    }
    public static void main()
    {
       Primepalin obj=new Primepalin();
       obj.accept();
    }
}
