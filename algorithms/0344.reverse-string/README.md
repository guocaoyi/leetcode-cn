# 344. Reverse String

Given an unsorted array return whether an increasing subsequence of length 3 exists or not in the array.

Formally the function should:

> Return true if there exists i, j, k
>
> such that arr[i] < arr[j] < arr[k] given 0 ≤ i < j < k ≤ n-1 else return false.

## Note

Your algorithm should run in O(n) time complexity and O(1) space complexity.

### Example

```bash
Input: [1,2,3,4,5]
Output: true
```

```bash
Input: [5,4,3,2,1]
Output: false
```

## Related Topics

- Binary Search
- Dynamic Programming

## Thinking

模拟 Array.reverse() 的实现；在

- 不得使用分配额外的空间
- 空间复杂度是 O(1) 的
- in-place algorithms

## Submissions

### I: Array.prototype.reverse

由于 Array 对象内置了 reverse 函数，先采用这个方法看看效率。然后自行实现 reverse

- Status: Accepted

```typescript
var reverseString = (s: string[]): void => {
  s.reverse();
};
```

### II: O(1) extra memory 迫使无法使用额外的数组进行缓存；

- Time: 2019.03
- Status: Wrong Answer
- Input: : `Input: ["h","e","l","l","o"] Output: ["h","e","l","l","o"] Expected: ["o","l","l","e","h"]`

```typescript
var reverseString = (s: string[]): void => {
  let arr: string[] = [];
  for (let i = s.length; i > 0; i--) {
    arr.push(s[i - 1]);
  }
  s = arr;
};
```

## Top Ranked
