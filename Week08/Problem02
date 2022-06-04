#include<iostream>
#include<bits/stdc++.h>


using namespace std;
int find(int s,int * parent)
{
    if(parent[s]<0)
    return s;
    return find(parent[s],parent);
}


void unionByweight(int s,int d,int*parent)
{
    int a=find(s,parent);
    int b=find(d, parent);
    
    if(a!=b)
    {
        if(a>b)
        {
           
            parent[b]+=parent[a];
             parent[a]=b;
           
        }
        else
        {
            
            parent[a]+=parent[b];
            parent[b]=a;
        }
       
    }
}
vector<pair<int,pair<int,int>>> krushkels(vector<pair<int,pair<int,int>>> &v,int vertex)
{
    vector<pair<int,pair<int,int>>> ans;
    int parent[vertex];
    for(int i=0;i<vertex;i++)
    {
        parent[i]=-1;

    }
  
    int s,d,w;
    sort(v.begin(),v.end());
    int E=v.size();
     

    for(int i=0;i<E;i++)
    {
        s=v[i].second.first;
        d=v[i].second.second;
        w=v[i].first;
         
        if(find(s,parent)!=find(d,parent))
        {
            ans.push_back(v[i]);
            unionByweight(s,d,parent);
        }
        
    }
   

    return ans;


}
int main(){
    int Ver,E;
     cout<<"enter the no. of vertex and edges\n";
    cin>>Ver>>E;
  vector<pair<int,pair<int,int>>> v,res;
  for(int i=0;i<E;i++)
  {
      int w,s,d;
      cin>>w>>s>>d;
       v.push_back(make_pair(w,make_pair(s,d)));
 
  }
  res=krushkels(v,Ver);

   
   int sum=0;
   
  for(int i=0;i<res.size();i++)
  {
     sum+=res[i].first;
     cout<<res[i].second.first<<"->"<<res[i].second.second<<"and-w--"<<res[i].first<<" ";
  }
    cout<<"\n\nThe minimum spanning tree sum:"<<endl;
   cout<<sum;

return 0;
}
