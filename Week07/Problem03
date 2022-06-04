#include <iostream>
#include <vector>
#include <stack>
#include<bits/stdc++.h>
using namespace std;
void search(vector<vector<int>> &v, int s, int des, int k,vector<int>&ans,int sum)
{
      if(k==0&&s==des)
      {ans.push_back(sum);
      return;}
      if(k==0||(k!=0&&s==des))
      return;
     for (int i = 1; i < v.size() + 1; i++)
            {
                if (v[s][i] != 0 )
                {
                   
                    search(v,i,des,k-1,ans,sum+v[s][i]);
                }
            }

}
int main()
{
    int n;
    cout << "enter the no. of nodes" << endl;
    cin >> n;
    vector<vector<int>> v(n + 1, vector<int>(n + 1, 0));

    for (int i = 1; i <= n; i++)
    {
        for (int j = 1; j <= n; j++)
            cin >> v[i][j];
    }
    int s, des, k;
    cin >> s >> des >> k;
    
    vector<int> ans;
    search(v, s, des, k,ans,0);
    cout<<*min_element(ans.begin(),ans.end());
    return 0;
}
