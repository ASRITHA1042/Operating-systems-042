#include<stdio.h>

int main()

{

	int i,j,n,p[10],bt[10],compt[10],temp1,temp2;	float sumwt=0.0,sumtat=0.0,wt[10],tat[10];

	printf("enter the number of processes:");

	scanf("%d",&n);

	printf("enter the burst time:");

	for(i=0;i<n;i++)

	{

		scanf("%d",&bt[i]);

	}

	printf("enter the priorities for processes:");

	for(i=0;i<n;i++)

	{

		scanf("%d",&p[i]);

	}

	for(i=0;i<n;i++)

	{

		for(j=i+1;j<n;j++)

		{

			if(p[i]>p[j])

			temp1=bt[i];

			bt[i]=bt[j];

			bt[j]=temp1;

			temp2=p[i];

			p[i]=p[j];

			p[j]=temp2;

		}

	}

	compt[0]=bt[0];

	wt[0]=0;

	for(i=1;i<n;i++)

	{

		compt[i]=bt[i]+compt[i-1];

	}

	for(i=0;i<n;i++)

	{

		tat[i]=compt[i];

		wt[i]=tat[i]-bt[i];

		sumwt+=wt[i];

		sumtat+=tat[i];

	}

	printf("\n AVG waiting time=%f",sumwt/n);

	printf("\n AVG total turn around time=%f",sumtat/n);

	return 0;

}
