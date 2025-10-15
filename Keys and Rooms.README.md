class Solution {
    public boolean canVisitAllRooms(List<List<Integer>> rooms) {
        Set<Integer> visited = new HashSet<>();
        Stack<Integer> stack = new Stack<>();
        stack.push(0);
        while(!stack.isEmpty()){
            int ul = stack.pop();
            visited.add(ul);
            for(int key : rooms.get(ul)){
                if(!visited.contains(key)){
                    stack.push(key);
                }
            }
        }
        return visited.size() == rooms.size();
    }
}
