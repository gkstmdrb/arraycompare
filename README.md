# arraycompare

### 자바 배열 알고리즘

<br><br>

![image](https://user-images.githubusercontent.com/114748816/224601022-d31d3a63-3402-422c-a0b4-5e173b191d7b.png)

먼저 a와 b를 비교해 같은지 분별하는 매서드를 생성해 준다. <br><br><br><br>

![image](https://user-images.githubusercontent.com/114748816/224600820-64a5b491-ffc1-47ff-815a-4251255ed4c0.png)

a의 길이와 b의 길이가 같지 않다면 main 메서드로 false를 보내 false 값을 출력한다. <br><br><br><br>

'![image](https://user-images.githubusercontent.com/114748816/224600855-d2f21dc6-1597-4b2f-aa38-fad252857ba5.png)

i에 0을 입력하고 i가 a의 길이보다 작다면 i값이 1만큼 증가한다.

	public class array  {
		static boolean equals(int [] a, int [] b) {
			if (a.length != b.length)		\\ a의 길이와 b의 길이가 같지 않다면
				return false;			\\ main 메서드로 false 값을 보낸다.
			
			for (int i=0; i < a.length; i++) 	\\ i에 0을 대입하고 i가 a의 길이보다 작다면 i값 증가
				if (a[i] != b[i])		\\ a배열의 길이와 b배열의 길이가 같지 않다면
					return false;		\\ main 메서드로 false 값을 보낸다.
			
			return true;				\\ 위에서 걸러지지 않았다면 main 매서드로 true 값을 보낸다.
		}
	
	
	
	
	public static void main(String[] args) {		\\ main 매서드
		// TODO Auto-generated method stub

		Scanner sc = new Scanner(System.in);		\\ Scanner sc를 만든다.
		
		System.out.println("배열의 a길이: ");
		int x = sc.nextInt();				\\ x 방에 입력한 값을 대입한다.
		int [] a = new int[x];		\\ int []은 정수형 배열을 선언, a는 배열의 이름, new int[x]는 x개의 정수를 저장할 수 있는 배열을 생성하는 것이다.
		
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

