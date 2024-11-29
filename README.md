#include <iostream>

using namespace std;

int main()
{
    //DECLARACION CHAR PARA DO-WHILE
    char continuar ;
    //DECLARACION DE DATOS FLOTANTES
    float V,P;
    //DECLARACION DE UN ENTERO
    int Vt=0;
    //DECLARACION UN ENTERO
    int Nvoltaje;


    //INICIO EL DO-WHILE
    do {
    cout << "INGRESE EL NUMERO DE VECES DE VOLTAJES QUE QUIERES CALCULAR" << endl;
    cin>> Nvoltaje;

    //ESTRUCTURA REPETITIVA DE FOR QUE INICIA EN 0 A Nvoltajes, SE INCREMENTA 1 CADA QUE PASA
    for (int i=0; i<Nvoltaje; i++ ){
    cout << "INGRESE EL VALOR DEL VOLTAJE "<<i<<":"<<endl;
    cin>>V;

    //CONDICON QUE EL VALOR INGRESADO DEL VOLTAJE DE ESTAR ENTRE 0 A 1000
    if (V>0 && V<1000){
     Vt = Vt+V;
        }
    else
    cout << "SU VOLTAJE NO CUMPLE CON LOS REQUISITOS"<<endl;
    }
    P = Vt/Nvoltaje;
    cout<< "*************************"<<endl;
    cout << "P DEL VOLTAJE ES: "<<P<<endl;
    cout << "Vt DEL VOLTAJE ES: "<<Vt<<endl;
    cout<< "*************************"<<endl;

    if (P<300){
    cout << "PROMEDIO DE VOLTAJE BAJO"<<endl;
    cout<< "-------------------------"<<endl;
    }
    else if (P>300 && P<700){

    cout<< "PROMEDIO DEL VOLTAJE ESTA EN EL RANGO"<<endl;
    cout<< "*************************"<<endl;

    }
    else
    cout<< "*************************"<<endl;
    cout<< "PROMEDIO DE VOLTAJE ES ALTO"<< endl;
    cout<< "*************************"<<endl;

    cout<< "DESEA CONTINUAR Y O N"<<endl;
    cin>> continuar;


    }while (continuar == 'Y');
    return 0;
}
