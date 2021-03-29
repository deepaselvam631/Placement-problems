#array 0's 1's and 2's problem:


class Solution {
    public void sortColors(int[] nums) {
        int low = 0;
        int mid = 0;
        int high = nums.length-1;
        int temp;
        
        while(mid <= high)
        {
            switch(nums[mid])
            {
                case 0:
                    temp = nums[low];
                    nums[low] = nums[mid];
                    nums[mid] = temp;
                    low++;
                    mid++;
                    break;
                    
                    
                case 1:
                    mid++;
                    break;
                
                case 2:
                    temp = nums[mid];
                    nums[mid] = nums[high];
                    nums[high] = temp;
                    high--;
                    break;
                    
            }
        }
    }
}
