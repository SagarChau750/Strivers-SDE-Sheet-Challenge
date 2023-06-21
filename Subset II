#include <bits/stdc++.h> 

void solve(int idx,vector<int>&temp,vector<vector<int>>&ans,vector<int>&arr,int n){
    ans.push_back(temp);

    if(idx >= n)
        return;
    for(int i = idx; i < n; i++){
        if(i > idx && arr[i] == arr[i-1])
            continue;

        temp.push_back(arr[i]);
        solve(i+1,temp,ans,arr,n);
        temp.pop_back();
    }
}

vector<vector<int>> uniqueSubsets(int n, vector<int> &arr){
    if(n==0)return{};

    sort(arr.begin(),arr.end());
    vector<int>temp;
    vector<vector<int>>ans;
    solve(0,temp,ans,arr,n);
    return ans;

}
