pointer-bsort
=============


//
//  main.cpp
//ptrsort.cpp
//shiyu

#include <iostream>
using namespace std;

int main()
{
    void bsort(int*, int);  //prototype
    const int N=10;
    
    int arr[N]={37,35,32,54,64,234,64,23,65,10};
    bsort(arr,N);
    
    for (int j=0; j<N; j++)
        cout<<arr[j]<<" ";
    cout<<endl;
    return 0;
}
//..........
void bsort(int* ptr, int n)
{
    void order(int*,int*);     //prototype
    int j,k;          //indexed to array
    
    for(j=0;j<n-1;j++)
        for (k=0;k<n;k++)
            order(ptr+j,ptr+k);     //order the pointer contents
}
//...................
void order(int* numb1,int* numb2)     //orders two numbers
{
    if (*numb1>*numb2) {
        int temp=*numb1;
        *numb1=*numb2;
        *numb2=temp;
        
    }
}
