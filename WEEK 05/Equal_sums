#include <iostream>
#include <time.h>
using namespace std;

// Functions for Quicksort 
void swap(int*, int*);
int pivot(int*, int, int);
void quicksort(int*, int, int);

void equalSum(int n, int arr[], int k)
{
    quicksort(arr, 0, n-1);
    int i=0, j=n-1, t, out=0;
    
     while(i<j)
      {
          if(v[i]+v[j]==k)
          {
              cout<<i<<"," <<j<<","<<k<<endl;
              out=1;
              break;
          }
          else if( k>v[i]+v[j])
           i++;
           else
           j--;
      }

    if(!out) 
        cout << "No such pair Exist";

    cout << endl;
}

int main()
{
    int t,n,i,k;
    cin >> t;
    while(t>0)
    {
        cin >> n;
        int arr[n];
        for(i=0; i<n; ++i)
        {
            cin >> arr[i];
        }
        cin >> k;

        equalSum(n, arr, k);   //Equal Sum
        --t;
    }
    return 0;
}

void swap(int* a, int* b)
{
    int temp=*a;
    *a=*b;
    *b=temp;
}

int pivot(int arr[], int st, int en)
{
    srand(time(0));
    int pivot_index = st + rand()%(en-st);

    swap(arr+pivot_index, arr+en);
    int pos=st, i;

    for(i=st; i<en; ++i)
    {
        if(arr[i]<=arr[en])
        {
            swap(arr+i, arr+pos);
            ++pos;
        }
    }
    swap(arr+pos, arr+en);
    return pos;
}

void quicksort(int arr[], int st, int en)
{
    if(st<en)
    {
        int mid = pivot(arr, st, en);

        quicksort(arr, st, mid-1);
        quicksort(arr, mid+1, en);
    }
}
