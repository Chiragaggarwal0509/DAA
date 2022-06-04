#include<iostream>
#include<vector>
#include<queue>
#include<bits/stdc++.h>
using namespace std;
 
 void dijkstra(vector<vector<int>>&v,int s,int n)
 {
     vector<int>dis(n+1,INT_MAX);
 
       vector<int> path[n+1];
 dis[s]=0;
   priority_queue<pair<int,int>>q;
   q.push({dis[s],s});
  
   
   while(!q.empty())
   {
       pair<int,int>a=q.top();
       q.pop();
       for(int i=1;i<=n;i++)
       {
           if(v[a.second][i]!=0&&a.first+v[a.second][i]<dis[i])
           {
               path[i].clear();
               for(int val:path[a.second])
               path[i].push_back(val);
               path[i].push_back(a.second);


               dis[i]=a.first+v[a.second][i];

               q.push({dis[i],i});
               
               
           }
       }
   }
   cout<<"the shortest distance of each vertex from source node is:"<<endl;
   for(int i=1;i<=n;i++)
   {
        cout<<i<<" ";
       for(int j=path[i].size()-1;j>=0;j--)
       cout<<path[i][j]<<" ";
       cout<<":"<<dis[i]<<"\n";}
 }
int main(){
int n;
cout<<"enter the no. of nodes"<<endl;
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
 dijkstra(v,source,n);
 
 
return 0;
}
