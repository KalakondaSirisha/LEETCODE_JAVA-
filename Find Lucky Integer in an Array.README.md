class Solution {
    public int findLucky(int[] arr) {
        Map<Integer, Integer> dict = new HashMap<>();
        for(int num : arr){
           dict.put(num, dict.getOrDefault(num, 0) + 1);
        }

        List<Integer> keys = new ArrayList<>(dict.keySet());

        int res = -1;
        for(int key : keys){
            if(key == dict.get(key)){
                res = Math.max(res, key);
            }
        }
        return res;
    }
}
