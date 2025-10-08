class Solution {
    public int longestOnes(int[] nums, int k) {
        int left = 0;
        int zcnt = 0;
        int maxLen = 0;
        int curLen = 0;

        for(int right = 0; right < nums.length; right++){
            if(nums[right] == 0){
                zcnt++;
            }
            while(zcnt > k){
                if(nums[left] == 0){
                    zcnt--;
                }
                left++;
            }
            curLen = right - left + 1;
            maxLen = Math.max(maxLen, curLen);
        }
        return maxLen;
    }
}
