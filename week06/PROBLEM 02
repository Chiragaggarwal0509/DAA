#include<iostream>
#include<vector>
#include<queue>
using namespace std;
 bool bfs(int s,vector<int>&color,vector<vector<int>>&v,int n)
 {
   queue<int>q;
   q.push(s);
   color[s]=1;
   while(!q.empty())
   {
       int a=q.front();
       q.pop();
       for(int i=0;i<n;i++)
       {
           if(v[a][i]!=0&&color[i]==-1)
           {
               q.push(i);
               color[i]=1-color[a];
           }
           else if(v[a][i]!=0&&color[i]==color[a])
           return false;
       }
   }
   return true;
 }
int main(){
int n;
cout<<"enter the no. of nodes"<<endl;
cin>>n;
vector<vector<int>>v(n,vector<int>(n,0));
 for(int i=0;i<n;i++)
 {
     for(int j=0;j<n;j++)
     cin>>v[i][j];
 }
 vector<int>color(n+1,-1);
 int f=0;
 for(int i=0;i<n;i++)
 {
     if(color[i]==-1)
   if ( !bfs(i,color,v,n))
        {
            f=1;
            cout<<"Not Bipartite";
            break;
        }}
 if(f==0)
 cout<<"Yes Bipartite"<<endl;
return 0;
}
