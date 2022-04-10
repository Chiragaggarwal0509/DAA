//Given an unsorted array implement bubble sort and find the no. of comparisions performed in it
#include<iostream>
using namespace std;
void bubblesort(int a[],int n)
{
    int f=0,swap=0,count=0;
    
    for(int i=0;i<n;i++)
    {
        f=0;
        
      
          for(int j=0;j<n-1-i;j++)
          {

              if(a[j]>a[j+1])
              {count++;
                  f=1;
                  int temp=a[j];
                  a[j]=a[j+1];
                  a[j+1]=temp;
              }
              
              
          }
          if(f==0)
          break;
         
    }
    cout<<count<<"--the no. of comparisons\n";
    
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
  bubblesort(a,n);
  for(int i=0;i<n;i++)
  {
      cout<<a[i]<<" ";
  }


return 0;
}
