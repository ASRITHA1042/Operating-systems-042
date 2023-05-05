#include <stdio.h>  

int main()  

{    

    int n, m, i, j, k,y; 

	int f[n], ans[n], ind = 0;  

    n = 3, m = 3,y=0;                         

    int alloc[3][3] = {{3,3,3},    

                       {2,0,3},      

                       {1,2,4}};   

    int max[3][3] = {{3,6,8},    

                     {4,3,3},      

                     {3,4,4}}; 

    int avail[3] = {1,2,0};  

    for (k = 0; k < n; k++)  

    {  

        f[k] = 0;  

    }  

    int need[n][m];  

    for (i = 0; i < n; i++)  

    {  

        for (j = 0; j < m; j++)  

            need[i][j] = max[i][j] - alloc[i][j];  

    }   

    for (k = 0; k <n; k++)  

    {  

        for (i = 0; i < n; i++)  

        {  

            if (f[i] == 0)  

            {  

                int flag = 0;  

                for (j = 0; j < m; j++)  

                {  

                    if (need[i][j] > avail[j])  

                    {  

                        flag = 1;  

                        break;  

                    }  

                }  

                if (flag == 0)  

                {  

                    ans[ind++] = i;  

                    for (y = 0; y < m; y++)  

                        avail[y] += alloc[i][y];  

                    f[i] = 1;  

                }  

            }  

        }  

    }  

    int flag = 1;  

    for (int i = 0; i < n; i++)  

    {  

        if (f[i] == 0)  

        {  

            flag = 0;  

            printf("system  not safe");  

            break;  

        }  

    }  

    if (flag == 1)  

    {  

        printf("safe system sequence\n");  

        for (i = 0; i < n - 1; i++)  

            printf(" P%d ->", ans[i]);  

        printf(" P%d", ans[n - 1]);  

    }  

    return (0);  

}
