class Solution {
    public int maxOperations(int[] nums, int k) {
        int cnt = 0;
        int left = 0;
        int right = nums.length - 1;
        Arrays.sort(nums);
        
        while(left < right){
            int total = nums[left] + nums[right];
            if(total == k){
                cnt++;
                left++;
                right --;
            }
            else if(total < k){
                left++;
            }
            else{
                right--;
            }
        }
        return cnt;
    }
}
