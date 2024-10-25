# Sorting & Searching Algorithms

## Binary Search

```java
    public int search(int[] nums, int target) {
        int left = 0;
        int right = nums.length - 1;

        while (left <= right) {
            int mid = (right + left) / 2;
            if (target == nums[mid]) {
                return mid;
            } else if (target > nums[mid]) {
                left = mid + 1;
            } else {
                right = mid - 1;
            }
        }

        return -1;
    }
```

## Breadth-First Search (BFS)

Normal

```java
    public void bfs(TreeNode node) {
        Queue<TreeNode> queue = new LinkedList<>();
        queue.add(node);

        while (!queue.isEmpty()) {
            TreeNode current = queue.poll();
            System.out.println(current.val);
            if (current.left != null) {
                queue.add(current.left);
            }
            if (current.right != null) {
                queue.add(current.right);
            }
        }
    }
```

Print each level

```java
    public void bfs(TreeNode node) {
        Queue<TreeNode> queue = new LinkedList<>();
        int level = 0;
        queue.add(p);

        while (!queue.isEmpty()) {
            System.out.println("level: " + level++);
            int size = queue.size();
            for (int i = 0; i < size; i++) {
                TreeNode current = queue.poll();
                System.out.println(current.val);
                if (current.left != null) {
                    queue.add(current.left);
                }
                if (current.right != null) {
                    queue.add(current.right);
                }
            }
        }
    }
```

## Depth-First Search (DFS)

Normal

```java
    public void dfs(TreeNode node) {
        if (node == null) { return; }
        System.out.println(node.val);
        dfs(node.left);
        dfs(node.right);
    }
```

Count depth

```java
    public int dfs(TreeNode node) {
        if (node == null) { return 0; }
        int left = dfs(node.left);
        int right = dfs(node.right);
        return Math.max(left, right) + 1;
    }
```

## Quick Sort

## Merge Sort

## Heap Sort

## Insertion Sort

## Selection Sort

## Bubble Sort

## Counting Sort

## Radix Sort

## Topological Sort (useful in graphs)
