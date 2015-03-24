# algoritmos-1#include "stdafx.h"
#include "conio.h"
#include <iostream>
#include <string>
# define tam 100

using namespace std;


int main()
{	int total;
	string nombres[tam], nombre, apellido;
 unsigned int encontro;
  do{
		cout<<"ingrese el numero de nombres: ";
		cin>> total;
  } while (!(total<= tam));	
		
	  cin.ignore();
   
    for (int i=0;i<total;i++)
	{
		cout<<"ingrese el "<<i+1<<"nombre: ";
		getline(cin, nombres[i]);
	}
	cout<<"\nResultados\n";
	for(int i=0;i<total;i++)
	{ encontro=nombres[i].find(' ');
	if (encontro !=string:: npos)
	{nombre=nombres[i].substr(0, encontro);
	 apellido=nombres[i].substr(encontro+1,nombres[i].length());
	 cout<<apellido<<",";
	 cout<<nombre<<endl;
	}
	}
	getch();
}
