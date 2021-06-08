# Third-assignment 


    #include <stdio.h>

  

    int main()
    {
    int X=3; 
        int A[X][X]; // Matrix 1 
        int B[X][X]; // Matrix 2
        int C[X][X]; // Resultant matrix

        int row, col, i, sum;
        for(row=0; row<SIZE; row++)
        {
            for(col=0; col<X; col++)
            {
                scanf("%d", &A[row][col]);
            }
        }

        
        printf("\nEnter elements in matrix B of size %dx%d: \n", X, X);
        for(row=0; row<X; row++)
        {
            for(col=0; col<X; col++)
            {
                scanf("%d", &B[row][col]);
            }
        }

        
        for(row=0; row<X; row++)
        {
            for(col=0; col<X; col++)
            {
                sum = 0;
                
                for(i=0; i<X; i++)
                {
                    sum += A[row][i] * B[i][col];
                }

                C[row][col] = sum;
            }
        }

       
        printf("\nProduct of matrix A * B = \n");
        for(row=0; row<X; row++)
        {
            for(col=0; col<X; col++)
            {
                printf("%d ", C[row][col]);
            }
            printf("\n");
        }

        return 0;
    } 
    
![Screenshot (3)](https://user-images.githubusercontent.com/85512440/121073133-9f753f00-c77e-11eb-8efa-7090b7b23ad5.png) 




                import java.util.Scanner;

                        class MatrixMultiplication
                        {
                           public static void main(String args[])
                           {
                              int a, b, p, q, sum = 0, c, d, k;

                              Scanner in = new Scanner(System.in);
                              System.out.println("Enter the number of rows and columns of first matrix");
                              a = in.nextInt();
                              b = in.nextInt();

                              int first[][] = new int[a][b];

                              System.out.println("Enter elements of the first matrix");

                              for (c = 0; c < a; c++)
                                 for (d = 0; d < b; d++)
                                    first[c][d] = in.nextInt();

                              System.out.println("enter the number of rows and columns of  the second matrix");
                              p = in.nextInt();
                              q = in.nextInt();

                              if (b != p)
                                 System.out.println("The matrices can't be multiplied with each other.");
                              else
                              {
                                 int second[][] = new int[p][q];
                                 int multiply[][] = new int[a][q];

                                 System.out.println("Enter elements of second matrix");

                                 for (c = 0; c < p; c++)
                                    for (d = 0; d < q; d++)
                                       second[c][d] = in.nextInt();

                                 for (c = 0; c < a; c++)
                                 {
                                    for (d = 0; d < q; d++)
                                    {  
                                       for (k = 0; k < p; k++)
                                       {
                                          sum = sum + first[c][k]*second[k][d];
                                       }

                                       multiply[c][d] = sum;
                                       sum = 0;
                                    }
                                 }

                                 System.out.println("Product of the matrices:");

                                 for (c = 0; c < a; c++)
                                 {
                                    for (d = 0; d < q; d++)
                                       System.out.print(multiply[c][d]+"\t");

                                    System.out.print("\n");
                                 }
                              }
                           }
                        } 
                        
                        
                        
                        
 ![Screenshot 06-08-2021 18 37 45 (2)](https://user-images.githubusercontent.com/85512440/121224840-6b108a00-c835-11eb-9749-6f5bc2f406c3.png)

