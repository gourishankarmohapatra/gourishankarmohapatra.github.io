# gourishankarmohapatra.github.io

import java.util.*;
import java.io.*;

class Xylem 
{
	public static void main(String[] args) 
	{
		int num, extreme_sum = 0, mean_sum = 0, n;   
		Scanner sc= new Scanner (System.in);  
		System.out.print("Enter a number: ");  
		
		num = sc.nextInt();  

		num = Math.abs(num);   
		n = num;    
		while(n != 0)  
		{    
		if(n == num || n < 10)  
//finds the last digit and add it to the variable extreme_sum  
		extreme_sum = extreme_sum + n % 10;  
		else  
//finds the mean digits and add it to the variable mean_sum  
		mean_sum = mean_sum + n % 10;  
//removes the last digit from the number  
		n = n / 10;  
		}  
		System.out.println("The sum of extreme digits: " + extreme_sum );  
		System.out.println("The sum of mean digits: " + mean_sum);  
//comparing the sum of extreme digits and with the sum of mean digits  
		if(extreme_sum  == mean_sum)  
//prints if sums are equal  
		System.out.println(num + " is a xylem number.");  
		else  
//prints if sums are not equal  
		System.out.println(num + " is a phloem number.");  
	}  
}  
