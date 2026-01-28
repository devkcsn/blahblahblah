class Solution {
    public int lengthOfLongestSubstring(String s) {
        // Use an array to store the last seen index of each character (ASCII chars)
        int[] lastSeen = new int[128]; // Can also use a HashMap
        int maxLength = 0;
        int left = 0; // Left bound of the sliding window

        // The right pointer 'right' is the loop variable
        for (int right = 0; right < s.length(); right++) {
            char currentChar = s.charAt(right);
            // Check if the current character was seen before within the current window
            if (lastSeen[currentChar] > left) {
                // If so, move the left pointer past the last occurrence of the character
                left = lastSeen[currentChar];
            }
            
            // Update the last seen position of the current character to its current index + 1
            // (storing 1-based index helps avoid issues with default 0 value)
            lastSeen[currentChar] = right + 1; 

            // Calculate the current window length and update the maximum length
            maxLength = Math.max(maxLength, right - left + 1);
        }

        return maxLength;
    }
}
