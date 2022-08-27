# maximum-minimum-in-an-array
Find the maximum and minimum value in an array













package javaCode1;
import java.util.*;

public class maxmANDminm {
	// find maxm and minm value in an array
//	static int maxm(int arr[] , int n ) {
//		int maxm = arr[0] ;
//		for(int i = 0 ; i<n ; i++ )//without using sorting
//		{
//			
//			if(arr[i]>maxm)
//				maxm = arr[i] ;
//		}
//		return maxm ;
//	}
//	static int minm(int arr[] , int n ) {
//		int minm = arr[0] ;
//		for(int i = 0 ; i<n ; i++ )//without using sorting
//		{
//			
//			if(arr[i]<minm)
//				minm = arr[i] ;
//		}
//		return minm ;
//	}
//Solving the same question using method Arrays.sort().
	
	static int maxm(int arr[] , int n) {
		Arrays.sort(arr); // arrange the array in ascending order
		int maxmVal = arr[n-1];
		int minmVal = arr[0] ;
		return maxmVal ;
		 
	}
	static int minm(int arr[] , int n ) {
		Arrays.sort(arr); // arrange the array in ascending order
		int minmVal = arr[0] ;
		return  minmVal ;
	}

	public static void main(String[] args) {
		Scanner sc = new Scanner(System.in) ;
		System.out.println("enter the size of array") ;
		int n = sc.nextInt();
		System.out.println("enter the elements of array") ;
		int arr[] = new int[n] ;
		for(int i = 0 ; i<n ; i++) {
			arr[i] = sc.nextInt() ;
		}
		int maxVal = maxm(arr , n) ;
		System.out.println(maxVal) ;
		int minVal = minm(arr , n) ;
		System.out.println(minVal) ;
		
		

	}

}
