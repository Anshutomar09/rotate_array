# rotate_array

class Solution {
public:
    void reverse( vector<int> &nums, int low, int high){
        while(low<high){
            swap(nums[low],nums[high]);
            low++;
            high--;
        }
    }
    void rotate(vector<int>& nums, int k) {
        int n=nums.size();
        k=k%n;
        reverse(nums, 0,n-k-1);//first group
        reverse(nums, n-k, n-1);//second group
        reverse(nums, 0, n-1);//whole array
        
    }
};
