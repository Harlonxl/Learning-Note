# Largest Rectangle in Histogram
题目描述：[Largest Rectangle in Histogram](https://www.lintcode.com/problem/largest-rectangle-in-histogram/description)
``` c++
// O(n)
class Solution {
public:
    /**
     * @param height: A list of integer
     * @return: The area of largest rectangle in the histogram
     */
    int largestRectangleArea(vector<int> &height) {
        if (height.size() == 0) {
            return 0;
        }
        
        stack<int> s;
        int largest = 0;
        
        for (int i=0; i<=height.size(); ++i) {
            int curt = i == height.size() ? -1 : height[i];
            while (!s.empty() && curt <= height[s.top()]) {
                int h = height[s.top()];
                s.pop();
                int w = s.empty() ? i : i - s.top() - 1;
                largest = max(largest, h * w);
            }
            s.push(i);
        }
        
        return largest;
    }
};
```