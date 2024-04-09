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
#  832. Flipping an Image](https://leetcode.com/problems/flipping-an-image/)
![[Pasted image 20240409091639.png]]
```java
class Solution {

    public int[][] flipAndInvertImage(int[][] image) {

     int[][] arr=new int[image.length][image[0].length];

     for(int i=0;i<image.length;i++){

        int k=0;

        for(int j=image[0].length-1;j>=0;j--){

            arr[i][k]=image[i][j];

            k+=1;

        }

     }

     for(int i=0;i<image.length;i++){

        int k=0;

        for(int j=0;j<image[i].length;j++){

          int result;

          result=(arr[i][j]==0)?1:0;

          arr[i][j]=result;

        }

     }

     return arr;

  

    }

}
```
# 1252. Cells with Odd Values in a Matrix](https://leetcode.com/problems/cells-with-odd-values-in-a-matrix/)
![[Pasted image 20240409100823.png]]
```java
class Solution {

    public int oddCells(int m, int n, int[][] indices) {

        int[][] arr = new int[m][n];

        for(int i=0;i<m;i++){

        for(int j=0;j<n;j++){

           arr[i][j]=0;

        }

     }

      for(int i=0;i<indices.length;i++){

        int j=0;

           int r = indices[i][j];

        for(int k=0;k<n;k++){

            arr[r][k]+=1;

           }

            j+=1;

           int p = indices[i][j];

        for(int k=0;k<m;k++){

            arr[k][p]+=1;

           }

        }

        int count=0;

          for(int i=0;i<m;i++){

        for(int j=0;j<n;j++){

            if(arr[i][j]%2!=0)

                count++;

        }

     }

     return count;

}

}
```
# 1572. Matrix Diagonal Sum](https://leetcode.com/problems/matrix-diagonal-sum/)
![[Pasted image 20240409110447.png]]
```java
class Solution {
    public int diagonalSum(int[][] mat) {
        int count=0;
        for(int i=0;i<mat.length;i++){
            count+=mat[i][i];
            mat[i][i]=0;
        }
        int k=0;
        for(int j=mat.length-1-k;j>=0;j--){
            count+=mat[k][j];
            mat[k][j]=0;
            k++;
        }
        return count;
    }
}
```
# 1295.Find Number with Even Number of digits(https://leetcode.com/problems/find-numbers-with-even-number-of-digits/description/)
![[Pasted image 20240409110614.png]]
```java
class Solution {

    public int findNumbers(int[] nums) {

        int count=0;

        for(int i=0;i<nums.length;i++){

            int k=0;

            while(nums[i]>0){

                nums[i]/=10;

                k+=1;

        }

        if(k%2==0)

            count+=1;

     }

     return count;

    }

}
```
# 867. Transpose Matrix](https://leetcode.com/problems/transpose-matrix/)
![[Pasted image 20240409122303.png]]
```java
class Solution {

    public int[][] transpose(int[][] matrix) {

        int[][] transpose=new int[matrix[0].length][matrix.length];

            for(int i=0;i<transpose.length;i++){

                for(int j=0;j<transpose[i].length;j++){

                    transpose[i][j]=matrix[j][i];

                }

            }

            return transpose;

    }

}
```
# 989. Add to Array-Form of Integer](https://leetcode.com/problems/add-to-array-form-of-integer/)
![[Pasted image 20240409143340.png]]
```java
class Solution {

    public List<Integer> addToArrayForm(int[] num, int k) {

    int s1=0,sum=0,temp=0,digit=0;

    for(int i=0;i<num.length;i++){

        s1=s1*10+num[i];

    }

    sum=s1+k;

    temp=sum;

    while(temp>0){

        temp/=10;

        digit+=1;

    }

    ArrayList<Integer> Num= new ArrayList<>();

    for(int i=0;i<digit;i++){

        int rem=sum%10;

        sum/=10;

    Num.add(rem);

    }

    Collections.reverse(Num);

    return Num;

    }

}
```