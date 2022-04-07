# Codeforcescpp-27A
#include <bits/stdc++.h>
using namespace std;

int main() {
	int n, nums[3001];
	cin >> n;
	for (int i = 0; i < n; i++)
		cin >> nums[i];
	sort(nums, nums + n);
	if (nums[0] > 1)
		cout << 1;
	else {
		int i = 1;
		while ((nums[i] - nums[i - 1]) == 1 && i < n) {
			i++;
		}
		cout << nums[i - 1] + 1;
	}
	return 0;
}
