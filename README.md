# Kadane-s-Algorithm
/*******
//Q.You need to find the maximum sum of a subarray (containing at least one element) in the array arr[].

Note : A subarray is a continuous part of an array

>>A Kadane's Algorithm is a dynamic programming algorithm used to find the maximum sum of a contiguous subarray within a one-dimensional array of numbers. It solves the "Maximum Subarray Problem" efficiently with a time complexity of O(n). 
*******/

class Solution {
public:
    int maxSubarraySum(vector<int>& arr) {
        int max_sum = arr[0];
        int current_sum =  arr[0];

        for (int i = 1; i < arr.size(); ++i) {
            current_sum = max(arr[i], current_sum + arr[i]);
            max_sum = max(max_sum, current_sum);
        }

        return max_sum;
    }
};
