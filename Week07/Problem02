#include<iostream>
#include<bits/stdc++.h>

using namespace std;
void bellmanFord(vector<vector<int>>v,int source,int n)
{
    vector<int>dis(n+1,INT_MAX);
    dis[source]=0;
    vector<int> path[n+1];
    for(int k=1;k<=n-1;k++)
    {
        for(int i=1;i<=n;i++)
        for(int j=1;j<=n;j++)
        {
            if(v[i][j]!=0&&dis[i]+v[i][j]<dis[j])
            {dis[j]=dis[i]+v[i][j];
            path[j].clear();
               for(int val:path[i])
               path[j].push_back(val);

               path[j].push_back(i);
               }
        }
    }
    int f=0;
     for(int i=1;i<=n;i++)
        for(int j=1;j<=n;j++)
        {
            if(v[i][j]!=0&&dis[i]+v[i][j]<dis[j])
            {
                f=1;
                break;
            }
        }
        if(f==1)
        cout<<"There is negative edge cycle present in the graph"<<endl;
    else
    {
        for(int i=1;i<=n;i++)
   {
        cout<<i<<" ";
       for(int j=path[i].size()-1;j>=0;j--)
       cout<<path[i][j]<<" ";
       cout<<":"<<dis[i]<<"\n";}
    }
}
int main(){
int n;
cout<<"Enter the no nodes"<<endl;
cin>>n;
vector<vector<int>>v(n+1,vector<int>(n+1,0));

 for(int i=1;i<=n;i++)
 {
     for(int j=1;j<=n;j++)
      cin>>v[i][j];
 }
 
 int source;
 cout<<"enter the source\n";
 cin>>source;
 bellmanFord(v,source,n);
 
return 0;
}
