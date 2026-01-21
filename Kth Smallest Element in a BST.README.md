class Solution {
    public int kthSmallest(TreeNode root, int k) {
        List<Integer> inorderlist = new ArrayList<>();
        inorder(root, inorderlist);
        return inorderlist.get(k - 1);
    }
    public void inorder(TreeNode root, List<Integer> inorderlist){
        if(root == null){
            return;
        }
        inorder(root.left, inorderlist);
        inorderlist.add(root.val);
        inorder(root.right, inorderlist);
    }
}
