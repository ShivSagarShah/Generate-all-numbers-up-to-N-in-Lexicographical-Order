#include<iostream>
using namespace std;

void lexi(int x, int n)
{
    //base case
    if(x>n) 
    return;
    
    if(x==n)
    {
        cout<<x<<endl;
        return;
    }
   
   //self work
    if (x!=0)
    cout<<x<<endl;
    
    //recursion
    for(int i=(x==0)?1:0; i<=9; i++)
    {
        lexi(10*x+i, n);
    }
}

int main()
{
    int n;
    cin>>n;
    lexi(0, n);
    return 0;
}
