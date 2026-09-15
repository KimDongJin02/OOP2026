# Homework1
```java
public class Homework1 {
    public static void main(String[] args) {
        int size = 10; 

      
        System.out.println("");
        for (int i = 1; i <= size; i++) {
            for (int j = 1; j <= i; j++) {
                System.out.print("#");
            }
            System.out.println();
        }

        
        System.out.println("\n");
        for (int i = size; i >= 1; i--) {
            for (int j = 1; j <= i; j++) {
                System.out.print("#");
            }
            System.out.println();
        }

       
        System.out.println("\n");
        for (int i = 1; i <= size; i++) {
           
            for (int j = 1; j <= size - i; j++) {
                System.out.print(" ");
            }
            
            for (int k = 1; k <= i; k++) {
                System.out.print("#");
            }
            System.out.println();
        }

        
        System.out.println("\n");
        for (int i = size; i >= 1; i--) {
            
            for (int j = 1; j <= size - i; j++) {
                System.out.print(" ");
            }
           
            for (int k = 1; k <= i; k++) {
                System.out.print("#");
            }
            System.out.println();
        }
    }
}
```
![Alt homework11](./images/homework1.png)


# Homework2
```java
public class Homework2 {
    public static void main(String[] args) {
        int n = 20;
        long[] fib = new long[n];

        fib[0] = 1;
        fib[1] = 1;

        for (int i = 2; i<n;i++){
            fib[i] = fib[i-1]+fib[i-2];
        }

        System.out.println("");
        for(int i=0;i<n;i++){
            System.out.print(fib[i]+(i==n-1?"":","));
        }
        System.out.println();
    }
}


```
![Alt homework21](./images/homework2.png)

# Homework3
```java
public class Homework3 {
    public static void main(String[] args) {
        int n = 21; 
        long[] fib = new long[n + 1];
        
        fib[1] = 1;
        fib[2] = 1;
        
        for (int i = 3; i <= n; i++) {
            fib[i] = fib[i - 1] + fib[i - 2];
        }
        
        for (int i = 1; i <= 20; i++) {
            double ratio = (double) fib[i + 1] / fib[i];
            System.out.printf("%2d | %d / %d \t\t\t| %.15f%n", i, fib[i + 1], fib[i], ratio);
        }
    }
}

```
![Alt homework31](./images/homework3.png)


# Homework4
```java
public class Homework4 {
	public static void main(String[] args) {

		
		for(int i=1; i < 10; i++) {
			System.out.println(i + "단을 출력 합니다.");
            
  	         	
			for(int j=1; j < 10; j++) {
				System.out.println(i + " x " + j + " = " + i * j);
			}
			System.out.println();
		}	
	}
}

```
![Alt homework41](./images/homework4.png)

# Homework5
```java
public class homework5 {
    public static void main(String[] args) {
        int iterations = 1000000; 

        double piLeibniz = calculateLeibniz(iterations);
        System.out.println("Gregory-Leibniz 공식 결과: " + piLeibniz);

        double piMadhava = calculateMadhava(iterations);
        System.out.println("Madhava 공식 결과: " + piMadhava);
        
        System.out.println("자바 내장 Math.PI 상수: " + Math.PI);
    }

  
    public static double calculateLeibniz(int limit) {
        double sum = 0.0;
        for (int i = 0; i < limit; i++) {
            
            double denominator = 2 * i + 1;
            
            if (i % 2 == 0) {
                sum += 4.0 / denominator;
            } else {
                sum -= 4.0 / denominator;
            }
        }
        return sum;
    }

    public static double calculateMadhava(int limit) {
        double sum = 0.0;
        for (int k = 0; k < limit; k++) {
            
            double numerator = Math.pow(-1.0 / 3.0, k);
            
            double denominator = 2 * k + 1;
            
            sum += numerator / denominator;
        }
        
        return Math.sqrt(12.0) * sum;
    }
}

```
![Alt homework51](./images/homework5.png)
