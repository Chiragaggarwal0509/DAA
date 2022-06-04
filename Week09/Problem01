#include<iostream>
#include<bits/stdc++.h>
 
using namespace std;
int main(){
int n;
cout<<"Enter the no. of the vertices in the graph "<<endl;
cin>>n;
vector<vector<int>>v(n,vector<int>(n,0));
cout<<"Enter the values in the matrix"<<endl;
for(int i=0;i<n;i++)
{
    for(int j=0;j<n;j++)
    {
        string s;
       cin>>s;
        if(s!="INF")
        {
           v[i][j]=stoi(s);
        }
        else
        v[i][j]=INT_MAX;
        
    }
}
for(int i=0;i<n;i++)
{
    for(int j=0;j<n;j++)
    {
        for(int k=0;k<n;k++)
        {

            if(v[i][j]>v[i][k]+v[k][j]&&v[i][k]!=INT_MAX&&v[k][j]!=INT_MAX)
            v[i][j]=v[i][k]+v[k][j];
        }
    }
}
cout<<"So the final anwer is:"<<endl;
for(int i=0;i<n;i++)
{
    for(int j=0;j<n;j++)
    {
        if(v[i][j]!=INT_MAX)
        cout<<v[i][j]<<" ";
        else
        cout<<"INF"<<" ";
        
           
    }
    cout<<"\n";
}
return 0;
}
