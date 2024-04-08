# 1920. Build Array from Permutation
![[Pasted image 20240319212449.png]]
```java
class Solution {

    public int[] buildArray(int[] nums) {

        // Scanner n= new Scanner(System.in);

        int[] arr= new int[nums.length];

        for(int i=0;i<nums.length;i++){

            arr[i]=nums[nums[i]];

        }

        return arr;

    }

}
```
# 1929. Concatenation of Array
![[Pasted image 20240319215420.png]]
```java
class Solution {

    public int[] getConcatenation(int[] nums) {

        int []arr= new int[nums.length*2];

        System.arraycopy(nums,0, arr, 0, nums.length);

        System.arraycopy(nums, 0, arr, nums.length, nums.length);

        return arr;

    }

}
```
# 1365. How Many Numbers Are Smaller Than the Current Number](https://leetcode.com/problems/how-many-numbers-are-smaller-than-the-current-number/)
![[Pasted image 20240408152908.png]]
```java
class Solution {

    public int[] smallerNumbersThanCurrent(int[] nums) {

        int [] arr = new int[nums.length];

        for(int i=0;i<nums.length;i++){

            int count=0;

            for(int j=0;j<nums.length;j++){

                if(nums[i]>nums[j])

                    count++;

            }

            arr[i]=count;

        }

        return arr;

    }

}
```
# 1389. Create Target Array in the Given Order](https://leetcode.com/problems/create-target-array-in-the-given-order/)
![[Pasted image 20240408155824.png]]
```java 
class Solution {

    public int[] createTargetArray(int[] nums, int[] index) {

        ArrayList<Integer> N = new ArrayList<>();

        for(int i=0;i<nums.length;i++){

        N.add(index[i],nums[i]);

    }

    for(int i=0;i<nums.length;i++){

         nums[i]=N.get(i);

    }

    return nums;

}

}
```