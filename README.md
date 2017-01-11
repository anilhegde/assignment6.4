package session6;

import java.util.Arrays;
import java.util.Random;
import java.util.Scanner;


public class Assignment64 {
	public static void main(String[] args) {
		int c, first, last, middle, n, search;
		Scanner sc= new Scanner(System.in);
		
	    int k=0;
	    int []array= new int[10];
	    Random rand = new Random();
		while(k!=9){
			array[k]=rand.nextInt(25);
			//System.out.println(array[k]);
			k=k+1;
		}
		Arrays.sort(array);
		
		System.out.println("Enter the number:");
		 search= sc.nextInt();
		
		first  = 0;
	    last   = 9;
	    middle = (first + last)/2;
	 
	    while( first <= last )
	    {
	      if ( array[middle] < search )
	        first = middle + 1;    
	      else if ( array[middle] == search ) 
	      {
	        System.out.println(search + " found at location " + (middle + 1) + ".");
	        break;
	      }
	      else
	         last = middle - 1;
	 
	      middle = (first + last)/2;
	   }
	   if ( first > last )
	      System.out.println(search + " is not present in the list.\n");
	   System.out.println("Elements in arrray are:");
	   for(int x:array){
			System.out.println(x);
		}
	}
	
	


}
