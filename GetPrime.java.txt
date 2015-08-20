import java.util.Scanner;

public class GetPrime {
	public static void main( String[] args ){
		Scanner kb = new Scanner(System.in);
		int low;
		int high;
		
		System.out.println("Low number");
		low = kb.nextInt();
		
		System.out.println("High number");
		high = kb.nextInt();
		
		for(int i=low;i<=high;i++){
			boolean isPrime = true;
			// Speed up by only searching up to the square root of the number
			int k = (int)(Math.sqrt(i))+1;
			for(int n=2;n<k;n++){
				if((i%n) == 0){ 
					isPrime = false;
					// Stop searching after we find a valid value
					break;
				}
			}
			if(isPrime){System.out.println(i);}
		}
	}
}