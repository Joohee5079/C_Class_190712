# C_Class_190712
주사위 게임



#include <stdio.h>
#include "stdlib.h"
#include "time.h"		//random number 처리 코드 1단계
void main()
{
	int my1, my2, com1, com2; //my=나, com=컴퓨터 
	srand((unsigned)(time(NULL)));//random number 처리 코드 2단계
	com1 = rand() % 6 + 1;		  //random number 처리 코드 3단계
	com2 = rand() % 6 + 1;
	my1 = rand() % 6 + 1;
	my2 = rand() % 6 + 1;
	printf("두 눈의 수 합이 높은 쪽이 이기는 게임\n주사위 게임 시작!\n--------------------------\n");
	printf("my  주사위 눈의 수 : %d, %d\n", my1, my2);
	printf("com 주사위 눈의 수 : %d, %d\n", com1, com2);
	printf("--------------------------\n");
	if (my1 == my2 && com1 != com2) printf("졌다!\n");
	else if (my1 != my2 && com1 != com2) printf("이겼다!\n");
	else if (my1 == my2 && com1 != com2 && my1 > com1) printf("졌다!\n");
	else if (my1 == my2 && com1 != com2 && my1 < com1) printf("이겼다!\n");
	else if (my1 == my2 && com1 != com2 && my1 == com1) printf("비겼다!\n");
	else if (my1 + my2 > com1 + com2) printf("졌다!\n");
	else if (my1 + my2 < com1 + com2) printf("이겼다!\n");
	else printf("비겼다!\n");
}
