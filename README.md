# ArrayStriver

Basic 
=====

1.LARGEST ELEMENT IN ARRAY
==========================
public class Solution {

    static int largestElement(int[] arr, int n) {
        
           
           int a=arr[0];
           for(int i=1;i<n;i++)
           {
               if(arr[i]>a)
               {
                   a=arr[i];
               }
           }
           return a;
    }
} 
