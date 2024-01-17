# ch04_java
package ch04_operator;

import java.util.Scanner;

public class OperatorEx {

	public static void main(String[] args) {
		// TODO Auto-generated method stub
		
	    //이메일 주소를 입력받고 @가 포함되어 있을경우
	      //(사용가능) 없을경우 (이메일형식이 아님)을 출력하시오.
	      //ex)ingdexOf는 대상문자열이 없을경우 -1 있을경우는 인덱스값을 반환함.
		
		//1.Scanner 생성
		//2.email입력 메시지 출력
		//3.입력받은 데이터를 가지고 비교 조건식작성
		//4.결과 출력
		
		Scanner scanner = new Scanner(System.in);
		 System.out.println("이메일을 입력해주세요");
		 System.out.print(">>>");
		 String id=scanner.nextLine();
		 String check = (id.indexOf("@") !=-1) ? ("사용가능") : ("이메일형식이 아님");
		 System.out.println(check);
		
	}

}


package ch04_operator;

import java.util.Scanner;

/**
 * Class Name : OperatorMain2024. 1. 3. Author : Kimgichan Created Date: 2024.
 * 1. 3. Version : 1.0 Purpose : operator study Descitption : 기본 연산자 공부
 */
public class OperatorMain {
	public static void main(String[] args) {
		// 연산자 operator
		// 1.중검 연산자
		int num = 10;
		num++;
		System.out.println(num);
		num--;
		System.out.println(num);
		int a, b;
		a = num++; // 후
		b = ++num; // 전
		System.out.printf("a:%d b:%d", a, b);
		System.out.println("\n ======== 산술 연산자 =====");
		int c = a * b;
		int d = a + b;
		System.out.printf("c:%d d:%d", c, d);
		System.out.println("\n나머지:" + (5 % 2));
		System.out.println("======== 대입 연산자 ========");
		num += 1;
		System.out.println(num);
		num *= 2;
		System.out.println(num);
		num /= 2;
		System.out.println(num);
		System.out.println("=======비교 연산자 ======");
		// 비교 경과에 따라 true/false 가 리턴됨.
		System.out.printf("a%d b:%d", a, b);
		System.out.println(a > b);
		System.out.println(a < b);
		System.out.println(a >= b);
		System.out.println(a <= b);
		System.out.println(a != b); // 같지 않다
		System.out.println(a == b); // 같다
		System.out.println("==========삼항 연산자 =======");
		// (a) ? (b) : (c) a의 조건식이 true이면 b 아니면 c
//		String id = "KimGiChan";
//		String check= (id.length() >=8) ? ("통과"): ("재입력");
//		System.out.println(check);
		Scanner scanner = new Scanner(System.in);
		System.out.println("아이디를 입력해주세요(8자 이상)");
		String id = scanner.nextLine();
		String check = (id.length() >= 8) ? ("통과") : ("재입력");
		System.out.println(check);
		System.out.println("성적을 입력해주세요");
		System.out.print(">>>");
//		int score = Integer.parseInt(scanner.nextLine());

		// 60 이상 통과 , 60미만 재시험을 줄력하시오!
		// sore 값을 가지고 삼항연산자를 이용하여 위의 조건에 따른 결과를 출력하시오.
//	     String msg=(score>=60) ? ("통과") : ("재시험");
//	     System.out.printf("%s 님은 %d점 으로 %s 입니다",id,score,msg);     
		// 사용자의 아이디는 8~14자리 이하일 경우만 가능!
		System.out.println("========= 논리 연산자 =======");
		// and -> && or ||
		System.out.println("아이디를 입력해주세요(8~14길이가능)");
		System.out.print(">>>");
		String str = scanner.nextLine();
		String msg = (str.length() >= 8 && str.length() < 15) ? "사용 가능한 아이디 입니다." : "8~14 자리로 입력하세요";
		System.out.println(msg);

		// 90 이상 A, 80 이상 B, 나머지C
		System.out.println("성정을 입력해주세요");
		System.out.print(">>>");
		int score = Integer.parseInt(scanner.nextLine());
		String grade = (score >= 90) ? ("A") : ((score >= 80) ? ("B") : ("C"));
		System.out.println(grade);

	}

}



