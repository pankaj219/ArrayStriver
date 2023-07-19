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


second largest and second smallest
==================================

import java.util.*;
import java.lang.*;
public class Solution {
    public static int[] getSecondOrderElements(int n, int []a) {
        
       int smallest = Integer.MAX_VALUE;
        int secondSmallest = Integer.MAX_VALUE;
        int largest = Integer.MIN_VALUE;
        int secondLargest = Integer.MIN_VALUE;
        
        for (int i = 0; i < n; i++) {
            int num = a[i];
            
            if (num < smallest) {
                secondSmallest = smallest;
                smallest = num;
            } else if (num < secondSmallest && num != smallest) {
                secondSmallest = num;
            }
            if (num > largest) {
                secondLargest = largest;
                largest = num;
            } else if (num > secondLargest && num != largest) {
                secondLargest = num;
            }
        }
        
        int[] result = {secondLargest, secondSmallest};
        return result;
    }
  }
