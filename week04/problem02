//. Given an unsorted array of integers, design an algorithm and implement it using a program to
//sort an array of elements by partitioning the array into two subarrays based on a pivot element
//such that one of the sub array holds values smaller than the pivot element while another sub
//array holds values greater than the pivot element. Pivot element should be selected randomly
//from the array. Your program should also find number of comparisons and swaps required for
//sorting the array.
#include <iostream>
using namespace std;
int partition(int a[],int p,int q,int* comparison)
{
    
    int x=a[p];
    int i=p;
    for(int j=p+1;j<=q;j++)
    {
       (*comparison)++;
        if(a[j]<=x)
        {
            i++;
            swap(a[i],a[j]);

        }

    }
    swap(a[p],a[i]);
    return i;
}
void quicksort(int a[],int p,int q,int * comparison)
{
    if(p<q)
    {
        int m=partition(a,p,q,comparison);
        quicksort(a,p,m-1,comparison);
        quicksort(a,m+1,q,comparison);
    }
}
int main()
{

    int n, t;
    cout << "Enter the no. of test cases\n";
    cin >> t;
    while (t--)
    {
        int a[30];
        cout << "Enter the no. of elements to be stored" << endl;
        cin >> n;
        for (int i = 0; i < n; i++)
        {
            int x;
            cin >> x;
            a[i] = x;
        }
        int comparison=0;
        //mergesort(a, 0, n - 1,&comparison);
        quicksort(a,0,n-1,&comparison);
         cout<<"no. of comparisons done are"<<comparison<<endl;
        for (int i = 0; i < n; i++)
        {
            cout << a[i] << " ";
        }
    }
    return 0;
}
