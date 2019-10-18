# print_diagonally

package elclipse;
import java.util.*;
public class Print_diagonally {

	public static void main(String[] args) {
		Scanner s=new Scanner(System.in);
		int m=s.nextInt();
		int n=s.nextInt();
		int matrix[][]= new int[m][n];
		for(int i=0;i<m;i++) {
			for(int j=0;j<n;j++) {
				matrix[i][j]=s.nextInt();                                                       //taking input from user
			}
		}

		for(int i=0;i<m;i++) {
			for(int j=0;j<n;j++) {
				System.out.print(matrix[i][j] + " ");                                          //printing the number
			}
			System.out.println();
		}
		printdiagonally(matrix,m,n);                                                      //calling the printdiagonally function
	}

	public static void printdiagonally(int matrix[][],int m,int n) {

		for(int k=0;k<=m-1;k++) {
			int i=k;
			int j=0;
			while(i>=0) {
				System.out.print(matrix[i][j] + " ");                                         //printing the matrix diagonally
				i=i-1;
				j=j+1;
			}
		}
		for(int k=1;k<=n-1;k++) {
			int i=m-1;
			int j=k;
			while(j<=n-1) {
				System.out.print(matrix[i][j] + " ");                                        //printing the matrix diagonally
				i=i-1;
				j=j+1;
			}
		}
	}
}

