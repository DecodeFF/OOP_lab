#include <iostream>
#include <math.h>
#include <fstream>
#include <stdio.h>
using namespace std;

class Myclass{
    public:
        double f(double x){
            return 4-x*x;
        }
    
    
    void func(){
        
    ofstream myFile("text.txt");
    double y;
    for (float x=-2;x<=2;x+=0.1)
    {
        if(x<-1.4)
        {
           y=2;
        }
        else if (x>=-1.4 && x<=-0.5)
        {
            y+=0.1;
        }
        else if (x>-0.5 && x<=0)
        {
            y+=0.2;
        }
        else if (x>0 && x<=0.5)
        {
            y-=0.2;
        }
        else if (x > 0.5 && x <=1.4)
            {
               y-=0.1;
            }

        else{
            y=2;
        }

        cout << " " << x << " , " << y << endl;
        myFile << " " << x << " , " << y << endl;
    }
        myFile.close();
    }
};
int main(){
   Myclass obj;

   obj.func();
   return 0;
}