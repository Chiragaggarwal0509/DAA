#include<iostream>
#include<vector>
using namespace std;
int main(){
    int n;
    cout<<"enter the nodes\n";
    cin>>n;

vector<vector<int>>v(n,vector<int>(n,0));
for(int i=0;i<n;i++)
{
    for(int j=0;j<n;j++)
    {
        cin>>v[i][j];
    }
}
vector<int>parent(n,-1);
vector<bool>mst(n,false);
vector<int>key(n,INT_MIN);
parent[0]=-1;
key[0]=0;
int i=0;
int sum=0;
while(i<n-1)
{
    int s,max=INT_MIN;
    
    for(int j=0;j<n;j++)
    {
       if(mst[j]==false&&max<key[j])
       {
           max=key[j];
           s=j;
       }
    }
       mst[s]=true;
       for(int j=0;j<n;j++)
       {
           if(v[s][j]&&mst[j]==false&&v[s][j]>key[j])
           {
               key[j]=v[s][j];
               parent[j]=s;
           }
       }
       i++;
    
}
for(int i=0;i<n;i++)
{cout<<parent[i]<<"-"<<i<<endl;
sum+=key[i];}
cout<<"The Maximum Spanning Tree is:"<<sum;



return 0;
}
