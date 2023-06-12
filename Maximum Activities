#include <bits/stdc++.h>
int maximumActivities(vector<int> &start, vector<int> &end) {

    int n = start.size();
    vector<pair<int,int>> v;
    for(int i=0;i<n;++i){
        v.emplace_back(make_pair(end[i],start[i]));
    }
    sort(v.begin(),v.end());
    int e = -1;
    int ans = 0;
    for(auto val : v){
        if(val.second>e-1){
            ans++;
            e = val.first;
        }
    }
    return ans;
}
