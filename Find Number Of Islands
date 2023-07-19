#include <bits/stdc++.h>
void dfs(int i, int j, vector<vector<int>> &vis, int** grid,
         int n, int m) {
  if (i < 0 || j < 0 || i >= n || j >= m)
    return;
  if (grid[i][j] == 0 || vis[i][j])
    return;
  vis[i][j] = 1;
  dfs(i + 1, j, vis, grid, n, m);
  dfs(i, j + 1, vis, grid, n, m);
  dfs(i - 1, j, vis, grid, n, m);
  dfs(i, j - 1, vis, grid, n, m);
  dfs(i + 1, j+1, vis, grid, n, m);
  dfs(i-1, j + 1, vis, grid, n, m);
  dfs(i - 1, j-1, vis, grid, n, m);
  dfs(i+1, j - 1, vis, grid, n, m);
}
int getTotalIslands(int** grid, int n, int m)
{
   // Write your code here.
   vector<vector<int>> vis(n,vector<int>(m,0));
        int count =0;
        for(int i=0; i<n; i++){
            for(int j=0; j<m; j++){
                if(!vis[i][j]&&grid[i][j]==1){                  
                    dfs(i,j,vis,grid,n,m);                    
                    count++;
                }
            }
        }        
        return count;
}
