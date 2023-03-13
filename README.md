# arraycompare

package project;
import java.util.Scanner;
public class arraycompare {

	public class array  {
		static boolean equals(int [] a, int [] b) {
			if (a.length != b.length)
				return false;
			
			for (int i=0; i < a.length; i++) 
				if (a[i] != b[i])
					return false;
			
			return true;
		}
	
	
	
	
	public static void main(String[] args) {
		// TODO Auto-generated method stub

		Scanner sc = new Scanner(System.in);
		
		System.out.println("배열의 a길이: ");
		int x = sc.nextInt();
		int [] a = new int[x];
		
		for (int i=0; i<x; i++) {
			System.out.println("a["+i+"]: ");
			a[i] = sc.nextInt();
		}
		System.out.println("배열의 b길이: ");
		int y = sc.nextInt();
		int [] b = new int[y];
		
		for (int i=0; i<x; i++) {
			System.out.println("b["+i+"]: ");
			b[i] = sc.nextInt();
		}
		
		System.out.println("배열 a와b는"+ (equals(a,b)?"같습니다.":"같지 않습니다."));
		
		}
	}
}
