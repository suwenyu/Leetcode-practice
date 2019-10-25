## Water Flowers (Google OA)

https://leetcode.com/discuss/interview-question/394347/

### Example
```
flowers = [2, 4, 5, 1, 2],
capacity1 = 5,
capacity2 = 7
```

### My Code
```c++
#include <iostream>
#include <vector>

using namespace std;

class Solution{
    public:
        int waterFlower(vector<int>flowers, int capacity1, int capacity2){
            if(flowers.size() == 0)
                return 0;
            int left = 0, right = flowers.size()-1;
            int ans = 0;
            int can1 = 0, can2 = 0;

            while(left < right){
                
                if(can1 < flowers[left]){
                    can1 = capacity1;
                    ans++;
                }
                if(can2 < flowers[right]){
                    can2 = capacity2;
                    ans++;
                }

                can1 -= flowers[left];
                can2 -= flowers[right];

                left++;
                right--;
            }
            if(can1 + can2 >= flowers[left])
                return ans;
            else
                return ans + 1;
        }
};


int main(void){

    vector<int>flowers = { 5, 5, 5, 5, 5, 10, 7, 7, 7, 7, 7 };
    int capacity1 = 5, capacity2 = 7;

    Solution sol;

    cout << sol.waterFlower(flowers, capacity1, capacity2) << endl;


    return 0;
}
```

### Others Solution
```c++
```

