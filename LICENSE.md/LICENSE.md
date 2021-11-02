#include<graphics.h>//header file for graphics coding
#include<iostream>//header file for c++ coding
#include<windows.h>//header file for all of the functions in the Windows API(Application Programming Interface)
#include<mmsystem.h>//header file for music system
int main()
{
	initwindow(800,500,"RAINBOW",150,50);
	readimagefile("rainbow2.jpg",100,0,700,50);
	
    for(int i=1;i<180;i++)//it is loop for 180 degree pixels colour setting
	{
		for(int j=1;j<=48;j++)//it is for filling colour in row pixels
		{
		setcolor(LIGHTMAGENTA);//colour setting
		arc(400,450,0,1+i,50+j);
		setcolor(LIGHTCYAN);
		arc(400,450,0,1+i,100+j);
		setcolor(LIGHTGRAY);
		arc(400,450,0,1+i,150+j);
		setcolor(LIGHTGREEN);
		arc(400,450,0,1+i,200+j);
		setcolor(LIGHTBLUE);
		arc(400,450,0,1+i,250+j);
		setcolor(YELLOW);
        arc(400,450,0,1+i,300+j);
		setcolor(LIGHTRED);
		arc(400,450,0,1+i,350+j);
    	}
		delay(1);
	}
	PlaySound(TEXT("R_S.wav"), NULL,SND_SYNC);
	system("pause");
	getch();
	closegraph();
}
