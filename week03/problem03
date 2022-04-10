//Given an unsorted array implement selection sort and find the no of comparisions and swaps done in it
#include<iostream>
using namespace std;
void selectionsort (int a[],int n)
{
    int pos,min=0,count=0,swap=0;
    for(int i=0;i<n-1;i++)
    {
        min=a[i];
        pos=i;
        for(int j=i+1;j<n;j++)
        {
            count++;
          if(min>a[j])
          {
              
              min=a[j];
              pos=j;
          }
        }
        if(pos!=i)
        {   swap++;
            a[pos]=a[i];
            a[i]=min;
        }
    }
    cout<<count<<" "<<"--the no. of comparison and "<<swap<<"--are the no. of swaps"<<endl;
}
int main(){
 int a[30];
  int n;
  
  cout<<"Enter the no. of elements to be stored"<<endl;
  cin>>n;
  for(int i=0;i<n;i++)
  {
      int x;
      cin>>x;
      a[i]=x;
  }
  selectionsort(a,n);
  for(int i=0;i<n;i++)
  {
      cout<<a[i]<<" ";
  }
return 0;
}
