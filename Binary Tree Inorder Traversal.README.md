class Solution {
    public List<Integer> inorderTraversal(TreeNode root) {
        List<Integer> result = new ArrayList<>();
        Traversal(root, result);
        return result;
    }
    private void Traversal(TreeNode node, List<Integer> result){
        if(node == null) return;
        Traversal(node.left, result);
        result.add(node.val);
        Traversal(node.right, result);
    }
}
