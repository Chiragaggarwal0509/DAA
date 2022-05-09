#include<bits/stdc++.h>
#include<iostream>
using namespace std;
void markvisited(int **g, int n , int k)
{
    for(int i = 0 ; i<n; i++)
        g[i][k]=2;
}
bool dfs(int **g, int n , int s, int d)
{
    vector<int> st;
    st.push_back(s);
    markvisited(g,n,s);
    while(!st.empty())
    {
        int x = st.back();
        st.pop_back();
        if(g[x][d]==1)
            return true;
        else
        {
            for(int i = 0 ; i<n; i++)
                if(g[x][i]==1)
                st.push_back(i);
            markvisited(g,n,x);
        }
    }
    return false ;
}
int main()
{
    int n ;
     cin>>n;
     int **arr;
     arr=(int**)malloc(n*sizeof(int *));
     for(int i = 0 ; i<n; i++)
     arr[i]=(int *)malloc(n*sizeof(int));
     for(int i = 0 ; i<n; i++)
     for(int j = 0 ; j<n ; ++j)
        cin>> arr[i][j];
     int s , d ;
     cin>>s>>d;
     bool ispresent=dfs(arr,n,s-1,d-1);
     if(ispresent)
     cout<<"yes path exits" << endl;
     else
        cout<<"no path"<<endl;
     return 0 ;
}
