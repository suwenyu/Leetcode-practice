# Leetcode Practice Records

##### Pratice Note
1. subarray sum -> presum array of hashmap

2. data stream題 -> 會需要class structure 並且define init function 與next function
ex:
```c++
class Solution{
    private:
        vector<int>nums;
    public:
        // constructor init array
        Solution(vector<int>nums){
            this->nums = nums;
        }
        // next function do when there are new data coming in.
        double next(vector<int>n){

        }
};
```

3. set intersection (function of c++)
```c++
#include <iostream>     // std::cout
#include <algorithm>    // std::set_intersection, std::sort
#include <vector>       // std::vector

using namespace std;

int main () {
    int first[] = {5,10,15,20,25};
    int second[] = {50,40,30,20,10};

    std::sort (first,first+5);     //  5 10 15 20 25
    std::sort (second,second+5);   // 10 20 30 40 50

    vector<int>tmp;

    set_intersection (first, first+5, second, second+5, back_inserter(tmp));
    cout << t << " ";
    cout << endl;

    return 0;
}

```

4. Minimax Alorithm

什么是Minimax，它是用在决策轮、博弈论和概率论中的一条决策规则。它被用来最小化最坏情况下的可能损失。“最坏”情况是对手带来的最坏情况，“最小”是我要执行的一个最优策略的目标。

Leetcode 486
```
f[i][j] = max(nums[i] + s[i+1][j], nums[j] + s[i][j-1]) 和 min(f[i+1][j], f[i][j-1])
```

Leetcode 375
Leetcode 464

5. 
用 pointer 的next or previous 要記得用=
ex.
```c++
it = next(it);
// and
it = prev(it);
```

6. 
sliding windows
two pointers right, left
if not enough, right++.
if too much, left++

ex:
1234. 992. 904. 1248.

7. subarray 的題
idea: sliding window, tow pointers, 
ex: subarray with k different (solution is to calculate the at most k difference and minus at most (k-1) difference)
一種是計算最多k個不同的字母的substring最長長度
另一種是substring有k個不同的字母 總共有多少substring

