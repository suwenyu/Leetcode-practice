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