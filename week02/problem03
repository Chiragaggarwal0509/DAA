//Find the count of pair whose difference is equal to the given key value
#include<iostream>
#include<vector>
using namespace std;
int main(){
  vector<int> v;
  int n;
  cout<<"enter the no. of elements"<<endl;
  cin>>n;
  for(int i=0;i<n;i++)
  {
      int a;
      cin>>a;
      v.push_back(a);
  }
  int key,count=0;
  cout<<"enter the key"<<endl;
  cin>>key;
  for(int i=0;i<n;i++)
  {
      for(int j=i;j<n;j++)
      {
          if(i!=j&&abs(v[i]-v[j])==key)
            count++;
      }
  }
  cout<<count<<" are the no. of pairs"<<endl;
return 0;
}
