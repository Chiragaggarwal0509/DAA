//Given an unsorted array implement insertion sort on it and find the no. of comparisions performed in this operation
#include<iostream>
using namespace std;
void insertion_sort(int a[],int n)
{
    int count=0;
    for(int i=1;i<n;i++)
    {
         int c=a[i];
         int j=i-1;
         while(c<a[j]&&j>=0)
         {
            count++;
             a[j+1]=a[j];
             j--;

         }
         a[j+1]=c;

    }
    cout<<count<<endl;
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
  insertion_sort(a,n);

  for(int i=0;i<n;i++)
  {
      cout<<a[i]<<" ";
  }
return 0;
}
