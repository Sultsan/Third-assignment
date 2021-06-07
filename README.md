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
