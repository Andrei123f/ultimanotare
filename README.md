# ultimanotare
ultima notare

#include <iostream>
#include<fstream>
using namespace std;
int v[100];
int n;
int tata;
int fiu;
int read_data()
{
    int i;
    fstream f("headinput.txt", ios::in);
    f>>n;
    for(i=1;i<=n;i++)
    {

        f>>v[i];
    }
    f.close();
}

int heap()
{
    int i;

for(i=2;i<=n;i++)
{
    int schimb;
    tata=i/2;
        
        while(v[tata]>v[i]&&v[tata]>1)
        {
            if(v[tata]>v[i])
            {
                v[tata]=schimb;
                v[tata]=v[i];
                schimb=v[i];


            }
            fiu=tata;
            tata=fiu/2;

        }

}
}
int print_data()
{
    int i;
    for(i=1;i<=n;i++)
    {

        cout<<"v["<<i<<"] = "<<v[i];
    }

}
int main()
{
read_data();
heap();
print_data();


}

