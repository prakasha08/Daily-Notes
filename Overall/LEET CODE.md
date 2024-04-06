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
![[Pasted image 20240319215420.png]]