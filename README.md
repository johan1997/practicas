# practicas
ejecicios resueltos
#include "stdafx.h"
#include <iostream>
#include "conio.h"
#include "stdlib.h"
#include <string>
#include "math.h"
using namespace std;
void nomap(string palabra,string palbra2);
int fact(int num);
float serie(int b);
void main()
{int opcion,fac,num,b;
float ser;
 string palabra,palabra2,cambio;
 do
 {cout<<"..............menu...................."<<endl;
  cout<<" 1.-cambiar posicion nombre y apellido"<<endl;
  cout<<" 2.-calcular factorial de un numero"<<endl;
  cout<<" 3.-cambiar posicion nombre y apellido"<<endl;
  cout<<" 4.-cambiar posicion nombre y apellido"<<endl;
  cout<<" 5.-cambiar posicion nombre y apellido"<<endl;
  cout<<"0.-salir"<<endl;
  cout<<" introdusca una opcion"<<endl;
  cin>>opcion;
  switch(opcion)
  {case 1:
   cout<<"ingrese el nombre"<<endl;
   cin>>palabra;
   cout<<endl;
   cout<<"ingrese el apellido"<<endl;
   cin>>palabra2;
   cout<<endl;
   nomap(palabra, palabra2);
   cout<<endl;
  
   break;
   case 2:
	   do
	   {cout<<"de que numero desea su factorial"<<endl;
	    cin>>num;
	   }while(num<0);
	   fac=fact( num);
	   cout<<"el factoria es: "<<fac;
	    cout<<endl;
	   break;

   case 3:
	    do
	   {cout<<"ingrece su base"<<endl;
	    cin>>b;
	   }while(b<0);
	    ser=serie(b);
		cout<<"el resultado es"<<ser;
		break;

   case 4:
   case 5:
   case 6:
	   cout<<"salir";
	   break;

   default:
	   cout<<"error";
	   break;
  }
  
 }while(opcion !=0);
 getch();
}
void nomap(string palabra,string palabra2)
{   
	string cambio ;
	cambio=palabra2+' '+palabra;
    cout<<endl;
    cout<<cambio;
   
}

int fact(int num)
{ int fac,p=1;
  if(num==0)
	  fac=1;
  else
	 { for(int i=1;i<=num;i++)
       {p=p*i;} 
   fac=p;
     }
    
  return fac;
}
float serie(int b)

{ float r,i;
  int f=1;
  for( i=1;i<=b;i++)
	 { f=f*i;
      r=(pow(b,i)/f);
     }
  return r;
}
