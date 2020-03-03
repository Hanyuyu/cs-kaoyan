# 排序
## 选择排序 - O(n^2)

```java
public static void selectionSort(Comparable[] arr){

        int n = arr.length;
        for( int i = 0 ; i < n ; i ++ ){
            // 寻找[i, n)区间里的最小值的索引
            int minIndex = i;
            for( int j = i + 1 ; j < n ; j ++ )
                // 使用compareTo方法比较两个Comparable对象的大小
                if( arr[j].compareTo( arr[minIndex] ) < 0 )
                    minIndex = j;

            swap( arr , i , minIndex);
        }
    }
```

> 思路: i=0 , 在[i, n)区间中选择一个最小的元素与区间左端元素交换位置

## 插入排序 - O(n^2) 不稳定

```java
public static void insertSort(Comparable[] arr){
    int n = arr.length;
    for(int i=0; i<n; i++){
        for(j=i;j>0 && arr[j]<arr[j-1];j--)
            swap(arr, j, j-1);
    }
}
