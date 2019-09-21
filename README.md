# amit
//Insertion sort 1

#include<iostream>
using namespace std;
int main()
{
    int n,i,x,ind,temp,j,temp1,k,flag;
    cin>>n;
    int a[n],b[n];
    for(i=0;i<n;i++)
    {
        cin>>a[i];
    }
    for(i=0;i<n;i++)
    {
        b[i]=a[i];
    }
    x=a[n-1];
    ind=n-1;
    for(i=n-2;i>=0;i--)
    {
        flag=0;
        if(x<a[i])
        {
            temp=a[i];
            a[i]=x;
            a[ind]=temp;
            b[ind]=b[i];
            ind=i;
            flag=1;
        }
        if(flag==1){
        for(j=0;j<n;j++)
        {
            cout<<b[j]<<" ";
        }
        cout<<endl;
        }
        for(k=0;k<n;k++)
        {
        b[k]=a[k];
        }
        
    }
    for(i=0;i<n;i++)
    {
        cout<<a[i]<<" ";
    }
    
    return 0;
}
