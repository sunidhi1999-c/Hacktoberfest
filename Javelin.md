/* package codechef; // don't place package name! */

import java.util.*;
import java.lang.*;
import java.io.*;
public class JavelinThrow {
    public static void main (String[] args) throws java.lang.Exception
    {
        // your code goes here
        Scanner s=new Scanner(System.in);
        int t=s.nextInt();
        while (t-->0){
            int n=s.nextInt();
            int m=s.nextInt();
            int x=s.nextInt();
            int[] arr=new int[n];
            int count=0,l=0;
            int[] ans=new int[n];
            for(int i=0;i<n;i++){
                arr[i]=s.nextInt();
                if(arr[i]>=m){
                    count++;
                    ans[l]=i+1;
                    l++;
                }

            }
            if(count==0){//Arrays.sort(arr);
                for(int i=0;i<n;i++){

                }
            }
            for(int i=0;i<count+1;i++){
                System.out.printf(count+" ");
            }

        }
    }
}


/* Name of the class has to be "Main" only if the class is public. */



