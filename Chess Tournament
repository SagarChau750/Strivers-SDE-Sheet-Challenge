#include <bits/stdc++.h>
bool canAssign(int c, int mid, vector<int> &positions) {
  int allot = 1, player = positions[0];
  for (int i = 1; i < positions.size(); i++) {
    if (positions[i] - player >= mid) {
      allot++;
      player = positions[i];
    }

    if (allot == c)
      return true;
  }

  return false;
}

int chessTournament(vector<int> &positions, int n, int c) {
  sort(positions.begin(), positions.end());
  int low = 1, high = positions[n - 1] - positions[0];
  int ans = -1;

  while (low <= high) {
    int mid = low + (high - low) / 2;
    if (canAssign(c, mid, positions)) { // minimum distance
      ans = mid;
      low = mid + 1;
    } else
      high = mid - 1;
  }
  return ans;
}
