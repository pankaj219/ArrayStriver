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


find duplicates element in an sorted array
===========================================


public class Solution {
	public static int removeDuplicates(ArrayList<Integer> arr,int n) {
		
		int i=0;
		for(int j=1;j<n;j++)
		{
			if(!arr.get(j).equals(arr.get(i)))
			{
               arr.set(i+1, arr.get(j));
			   i++;
			}
		}
		return (i+1);
	}
     }



left rotate an array by one place 
==================================



public class Solution {

    static int[] rotateArray(int[] arr, int n) {
        
        int temp=arr[0];
        for(int i=0;i<n-1;i++)
        {
            arr[i]=arr[i+1];
        }
        arr[n-1]=temp;
        return arr;

    }
     }

Move all zeros to the end without disturbing order of non zero element 
======================================================================

public static int[] moveZeros(int n, int []a) {
        
        int j=-1;
        for(int i=0;i<n;i++)
        {
            if(a[i]==0)
            {
                j=i;
                break;
            }
        }
        for(int i=j+1;i<n;i++)
        {
            if(a[i]!=0)
            {
                int temp=a[i];
                a[i]=a[j];
                a[j]=temp;
            }
        }
        return a;
    }
   }

Linear Search
=============

  public static int linearSearch(int n, int num, int []arr){
       
       for(int i=0;i<n;i++)
       {
           if(arr[i]==num)
           {
               return i;
           }
           
       }
       return -1;
     }
