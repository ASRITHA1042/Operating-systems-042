#include<stdio.h>

struct PSJF

{

    int wt,at,bt,tat;

};

struct PSJF a[10];

int main()

{

    int n,temp[10];

    int count=0,t=0,sp;

    float twt=0, ttat=0,awt,atat;

    printf("process no= ");

    scanf("%d",&n);

    printf("AT AND BT \n");

    for(int i=0;i<n;i++)

    {

    	printf("AT = ") ;        scanf("%d",&a[i].at);

        printf("BT = ");

        scanf("%d",&a[i].bt);

        temp[i]=a[i].bt;

    }

    a[9].bt=10000;

    for(t=0;count!=n;t++)

    {

        sp=9;

        for(int i=0;i<n;i++)

        {

            if(a[i].bt<a[sp].bt && (a[i].at<=t && a[i].bt>0))

            {

                sp=i;

            }  

        }

        a[sp].bt=a[sp].bt-1;

        if(a[sp].bt==0)

        {

            count++;

            a[sp].wt=t+1-a[sp].at-temp[sp];

            a[sp].tat=t+1-a[sp].at;

            twt=twt+a[sp].wt;

            ttat=ttat+a[sp].tat;

        }

    }

    awt=twt/n;

    atat=ttat/n;

    printf("p       WT       TAT\n");

    for(int i=0;i<n;i++)

    {

        printf("%d\t%d\t%d\n",i+1,a[i].wt,a[i].tat);

    }

    printf("Avg waiting time = %f\n",awt);

    printf("Avg turn around time =\n",atat); 

}
