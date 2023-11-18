# Find-the-Difference-of-Two-Arrays-using-Java-Leetcode


    class Solution {
        public List<List<Integer>> findDifference(int[] nums1, int[] nums2) {
            List<List<Integer>> list = new ArrayList<>();    
            Set<Integer> set1 = new HashSet<>();
            for(int num : nums1){
                set1.add(num);
            }
            Set<Integer> set2 = new HashSet<>();
            for(int num : nums2){
                set2.add(num);
            }
            List<Integer> left = new ArrayList<>();
            for(int num: set1){
                if(set2.contains(num)==false){
                    left.add(num);
                }
            }
            List<Integer> right = new ArrayList<>();
            for(int num: set2){
                if(set1.contains(num)==false){
                    right.add(num);
                }
            }
            list.add(left);
            list.add(right);
            return list;
        }
    }
