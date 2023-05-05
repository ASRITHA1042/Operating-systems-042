#include<stdio.h>

void firstfit(int blocksize[], int m, int processsize[], int n)

{

    int i, j;

    int allocation[n];

    for(i = 0; i < n; i++)

    {

        allocation[i] = -1;

    }

    for (i = 0; i < n; i++)        

    {

        for (j = 0; j < m; j++)        

        {

            if (blocksize[j] >= processsize[i])

            {

                allocation[i] = j;

                blocksize[j] -= processsize[i];

                break;   

            }

        }

    }

    printf("\nprocess No.\tprocess size\tblock no.\n");

    for (int i = 0; i < n; i++)

    {

        printf(" %i\t\t\t", i+1);

        printf("%i\t", processSize[i]);

        if (allocation[i] != -1)

            printf("%i", allocation[i] + 1);

        else

            printf("Not Allocated");

        printf("\n");

    }

}

int main()

{

    int m,n;     

      int blocksize[] = {300,600,350,200,750,125};

    int processsize[] = {115,500,358,200,375};

    m = sizeof(blocksize) / sizeof(blocksize[0]);

    n = sizeof(processsize) / sizeof(processsize[0]);

    firstfit(blocksize, m, processsize, n);

    return 0 ;

}
