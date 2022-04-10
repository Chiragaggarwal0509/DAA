//Given an unsorted array of positive integers, design an algorithm and implement it
//using a program to find whether there are any duplicate elements in the array or not.
//(use sorting) (Time Complexity = O(n log n))
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
void check_duplicate(int a[],int n)
{
    int i=0,j=n-1;
     while(i<j)
     {
         int mid=i+(j-i)/2;
         if(a[mid]==a[mid+1]||a[mid]==a[mid-1])
         {
             cout<<"YES";
             return;
         }
         
     }
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
  check_duplicate(a,n);
  for(int i=0;i<n;i++)
  {
      cout<<a[i]<<" ";
  }
return 0;
}
