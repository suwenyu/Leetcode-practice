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
