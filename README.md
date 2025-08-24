class Solution {
    public boolean isSubsetSum(int[] arr, int target) {
        //code
        return helper(0,0,arr,target);
      
    }
        // recursive helper function
    static boolean helper(int index,int currSum, int arr[], int target){
        int n = arr.length;
        
        
        //base case
        if(index == n){
            return currSum == target; // check if we reached target
        }
        
        
        //Pick the element code:
        if(helper(index+1,currSum + arr[index],arr, target))  return true;
        
        
        
        //Do not pick the element code:
        if(helper(index+1,currSum,arr,target)) return true;
        
        
        
        return false;
        
        
    }
}
