# Pink-Floyd

import java.util.*;
import javax.lang.model.util.ElementScanner6;
class Pink
{
    public static void main(String[] args)
    {
        Scanner scanner=new Scanner(System.in);
        int n=scanner.nextInt();
        int arr[]=new int[n];
        for(int i=0;i<n;i++)
        {
            arr[i]=scanner.nextInt();
        }
        int stack[]=new int[n];
        int exp=1;
        int count=0,top=-1;
        for(int i=0;i<n;i++)
        {
             while(top!=-1 && stack[top]==exp)
        {
        top--;
        count++;
         exp++;
      }
     if(arr[i]==exp)
    {
       count++;
       exp++;
    
    }
    else 
    {
        top=top+1;
        stack[top]=arr[i];
    }
}
 
if(top!=-1)
{
    while(top!=-1)
    {
        if(stack[top]!=exp)
        {
           
            break;
        }
        else
        {
            top=top-1;
            count++;
            exp++;
        }
    }
 
}
 
if(count==n)
System.out.println("Happy");
else
System.out.println("Sad");
}
}


