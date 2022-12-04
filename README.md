# recursive-obeb-okek-bulma
#include<stdio.h>
int obeb(int x,int y);
int okek(int x,int y);

int main(void)
{
	int sayi1,sayi2,sonuc1,sonuc2;
	printf("lütfen iki sayi giriniz");
	scanf("%d%d",&sayi1,&sayi2);
	sonuc1=okek(sayi1,sayi2);
	sonuc2=obeb(sayi1,sayi2);
	printf("girilen sayilarin okeki %d dir\n",sonuc1);
	printf("girilen sayilarin obebi %d dir\n",sonuc2);
	return 0;
}

int okek(int x,int y)
{
	return x*y/obeb(x,y);
}

int obeb(int x,int y)
{
	if(y==0)
	return x;
	return obeb(y,x%y);
}
