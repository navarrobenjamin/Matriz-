# Matriz-
Trabajo de la universidad
<img src="/docs/2x2.jpg" alt="My cool logo"/>


public static void Main(string[] args)
    {
        int[,] matrix = { { 2, 5, 7 },
                          { 3, 4, 5 },
                          { 4, 1 ,3 } };
        maxSubmatrixSum(matrix);
     }
     static void maxSubmatrixSum(int[,] matrix)
     {
         int r = matrix.GetLength(0);
         int c = matrix.GetLength(1);
         
         int max = 0;
         
         
        for (int i = 0; i < r-1; i++)
        {
             for (int j = 0; j < c-1; j++)
             {
                  int maxSubmatrix =matrix[i,j]+  matrix[i,j+1] + matrix[i+1,j]+matrix[i+1,j+1];
                  
                  Console.WriteLine();
                 
                  Console.Write(matrix[i,j]+" "+matrix[i,j+1]);
                  Console.WriteLine();
                  
                  Console.Write(matrix[i+1,j]+" "+matrix[i+1,j+1]);
                  Console.WriteLine();
                  
                if (maxSubmatrix > max)
                {
                   max = maxSubmatrix;
                }                
              }
         }
          Console.WriteLine();
        Console.WriteLine("El valor mas alto de las sumas al recorrer las matrices de 2x2 es: "+max);
    }
