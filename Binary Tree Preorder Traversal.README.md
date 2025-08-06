class Solution {
    public List<Integer> preorderTraversal(TreeNode root) {
        List<Integer> result = new ArrayList<>();
        Traversal(root, result);
        return result;
    }
    private void Traversal(TreeNode node, List<Integer> result){
        if(node == null) return;
        result.add(node.val);
        Traversal(node.left, result);
        Traversal(node.right, result);
    }
}
