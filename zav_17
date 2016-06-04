#include <stdio.h>
#include <stdlib.h>
#include <time.h>

#define SIZE 20
#define DIAP 30

void print_mas(int *mas, int n);
int perev(int *mas, int n, int zn);
void rand_mas_n(int *mas, int n, int kol, int poch);

/* run this program using the console pauser or add your own getch, system("pause") or input loop */

int main(int argc, char *argv[]) {
	
	int masA [2 * SIZE], masB[SIZE];
	int i, i_B, i_pr;
	int flag, siz_kol = 0;
	
	srand(time(0));
	
	rand_mas_n(masA, SIZE, DIAP, 0);
	rand_mas_n(masB, SIZE, DIAP, 0);
	printf("Massiv A:\n");
	print_mas(masA, SIZE);
	printf("Massiv B:\n");
	print_mas(masB, SIZE);
	
	for(i = SIZE, i_B = 0; i_B < SIZE; i_B++) {
		for(i_pr = 0, flag = 1; i_pr < SIZE; i_pr++) {
			if(masB[i_B] == masA[i_pr]) {
				flag = 0;
				break;
			}	
		}
		if(flag) {
			masA[i] = masB[i_B];
			siz_kol = siz_kol + 1;
			i++;
		}
	}
	
	printf("\nOb'edineni massivu:\n\n");
	print_mas(masA, SIZE + siz_kol);

	system("pause");
	return 0;
}

void print_mas(int *mas, int n){
	int i;
	for(i = 0; i < n; i++)
		printf("\tmas[%d] = %d\n", i, mas[i]);
}

int perev(int *mas, int n, int zn){
	int i;
	for(i = 0; i < n; i++)
		if(zn == mas[i])
			return 0;
		
	return 1;	
}

void rand_mas_n(int *mas, int n, int kol, int poch){
	int i;
	for(i = 0; i < n; ) {
		mas[i] = poch + rand() % kol;
		if(perev(mas, i, mas[i]))
			i++;
	}	
}
