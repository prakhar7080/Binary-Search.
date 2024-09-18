//# Binary-Search.
#include<iostream>
using namespace std;

bool binary_search(int a[], int n, int target) {
    int s = 0, e = n - 1;
    while (s <= e) {
        int mid = s + (e - s) / 2;
        if (a[mid] == target)
            return true;
        else if (target>a[mid])
            s = mid + 1;
        else
            e = mid - 1;
    }
}

int main() {
    int a[7] = {10, 20, 30, 40, 50, 60, 70};
    int n = 7;
    int target = 50;
    bool ans = binary_search(a, n, target);
    
    if (ans)
        cout << "Element present" << endl;
    else
        cout << "Element not present" << endl;
}
