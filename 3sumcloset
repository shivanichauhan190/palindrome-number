public class Solution {
    public int threeSumClosest(int[] nums, int target) {
        int minimalDist = Integer.MAX_VALUE;
        int res = 0;
        Arrays.sort(nums);

        for(int i=0;i<nums.length-2; i++){
            int l = i+1;
            int r = nums.length-1;
            while(l < r){
                int sum = nums[i] + nums[l] + nums[r];
                if(sum == target) return target;
                else if(sum > target){//pay attention how target and sum is handled here.
                    if((sum - target) < minimalDist){
                        minimalDist = sum - target;
                        res = sum;
                    }
                    r--;
                }else{
                    if((target - sum) < minimalDist){

                        minimalDist = target - sum;
                        res = sum;
                    } 
                    l++;
                }
            }
            while(i<nums.length -1 && nums[i] == nums[i+1]) i++;
        }

        return res;
    }

}
