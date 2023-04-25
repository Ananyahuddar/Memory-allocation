#include <stdio.h>
#include <stdlib.h>


int main()
{
	int *p; int *p2;
	p = (int*)malloc(2*sizeof(int));
	
	*p = 13;
	printf("The element allocated is %d \n",*p);
	
	p++;
	
	*p = 7;
	printf("The element allocated is %d \n",*p);
	
	p2 = (int*)realloc(p,sizeof(int));
	*p2 = 5;
	printf("The element allocated is %d \n",*p2);

	return 0;
}
