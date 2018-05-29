## 771. Jewels and Stones

You're given strings J representing the types of stones that are jewels, and S representing the stones you have.  Each character in S is a type of stone you have.  You want to know how many of the stones you have are also jewels.

The letters in J are guaranteed distinct, and all characters in J and S are letters. Letters are case sensitive, so "a" is considered a different type of stone from "A".

```
Input: J = "aA", S = "aAAbbbb"
Output: 3
```

### my code

```c++
class Solution {
public:
    int numJewelsInStones(string J, string S) {
        int sum = 0;
        for(int i=0 ; i< J.size();i++){
            for(int j=0 ; j < S.size() ; j++){
                if(J[i]==S[j]){
                    cout << J[i] << "," << S[j] << endl;
                    sum += 1;
                }
            }
        }
        return sum;
    }
};
```

### fastest solution
```c++
int numJewelsInStones(char* J, char* S) {
    int counter[256];
    for (register int i = 0; i < 256; i++) {
        counter[i] = 0;
    }
    
    for (register int i = 0; J[i] != '\0'; i++) {
        counter[(int)J[i]] = 1;
    }
    
    int ans = 0;
    for (register int i = 0; S[i] != '\0'; i++) {
        if (counter[(int)S[i]]) {
            ans++;
        }
    }
    return ans;
}
```


