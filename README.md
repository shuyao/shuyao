#include <stdio.h>
#include <stdlib.h>
#include <string.h>
int main()
{
	FILE *fp;
	printf("please input two numbers(seperated by key space):\n");
	int i,j; int*str2; 
	scanf("%d%d",&i,&j);
	printf("%d*%d=%d\n",i,j,i*j);      
	printf("please input the file name:\n");	
	char str[10];
	scanf("%s",str);
	if((fp=fopen("D:\\text.txt","a+"))==NULL)
	{
		printf("\ncannot open the file!!!");
		getchar();
		exit(1);
	}
	    fprintf(fp,"%d*%d=%d",i,j,i*j);
	    fclose(fp);
	 
}
