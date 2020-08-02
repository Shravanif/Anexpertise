import java.util.Scanner;


public class build
{ 
	
	static final int M=2; 
	static final int N=2;

	
	
	
	static int contribution_height(int current, int previous) 
	{ 
		return Math.abs(current - previous); 
	} 
	
	
	static int surfaceArea(int A[][]) 
	{   
		
		
		int ans = 0; 
	
		
		for (int i = 0; i < N; i++) 
		{ 
			for (int j = 0; j < M; j++) { 
	
			
				int up = 0; 
	
				
				int left = 0; 
	
				
				if (i > 0) 
					up = A[i - 1][j]; 
	
				 
				if (j > 0) 
					left = A[i][j - 1]; 
	
				
				ans += contribution_height(A[i][j], up) 
					+ contribution_height(A[i][j], left); 
	
				
				if (i == N - 1) 
					ans += A[i][j]; 
	
				
				if (j == M - 1) 
					ans += A[i][j]; 
			} 
		}
		ans+=N*4*2;
		return ans; 
	
		
		
	} 
	

	public static void main (String[] args) 
	{ 
		 Scanner scan = new Scanner(System.in);

	        System.out.println("Please Enter Number Of Buildings :");
	        int n = scan.nextInt();
	        
	        
	        for (int i = 0; i < n; i++) {
	        	System.out.println("Please Enter Building coordinates :" + (i+1));
	        	double xpoint = scan.nextDouble(), ypoint = scan.nextDouble();
	        	
	        }
	        double a=4.0+4.0;
	        System.out.println("Please Enter coordinates of S point :");
	        double p1 = scan.nextDouble(), p2 = scan.nextDouble();
	        
	      
	       
	        if ((surfaceArea(n))) 
	        { 
	            System.out.println(a); 
	        }  
	         
	        else  {
	        	 System.out.println("to be calculated"); 
	        }
	    }


	
	


	private static boolean surfaceArea(int n1) {
		
		return true;
	}




}