#include<iostream>
#include<vector>
#include<algorithm>
using namespace std;
bool cmp(pair<int,int>a,pair<int,int>b)
{
    return a.first*b.second>a.second*b.first;
}
int main(){
int n;
cin>>n;
vector<pair<int,int>>v(n);
for(int i=0;i<n;i++)
{
    cin>>v[i].first;
    cin>>v[i].second;
}
int w;
cin>>w;
sort(v.begin(),v.end(),cmp);

double profit=0;
for(int i=0;i<n;i++)
{
   if(w>v[i].second)
   {
      profit+=v[i].first;
      w-=v[i].second; 
   }
   else{
       profit+=w*((1.0*v[i].first)/(1.0*v[i].second));
       break;
   }
}
cout<<profit<<" ";

return 0;
}
