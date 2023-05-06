#include<stdio.h>  
#include<stdlib.h>  
#include<unistd.h>  
#include <sys/ipc.h>
#include<sys/shm.h>  
#include<string.h>  
int main()  
{  
int i;  
void *SM;  
char buff[100];  
int shmid;  
shmid=shmget((key_t)2345, 1024, 0666|IPC_CREAT);   
printf("key of shared memory is %d\n",shmid);  
SM=shmat(shmid,NULL,0);    
printf("process attached at %p\n",SM);    
printf("enter data  to shared memory \n");  
read(0,buff,100); 
strcpy(SM,buff);   
printf("IPC data using shared memory is %s\n",(char *)SM);  
}
