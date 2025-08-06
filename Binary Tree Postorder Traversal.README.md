class Solution {
    public List<Integer> postorderTraversal(TreeNode root) {
        List<Integer> result = new ArrayList<>();
        Traversal(root, result);
        return result;
    }
    private void Traversal(TreeNode node, List<Integer> result){
        if(node == null) return;
        Traversal(node.left, result);
        Traversal(node.right, result);
        result.add(node.val);
    }
}
