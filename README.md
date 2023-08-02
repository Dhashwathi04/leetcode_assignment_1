# leetcode_assignment_1

Roaman to Integer-----------------------------------------------
class Solution:
    def romanToInt(self, s):
        roman = {
            "I": 1,
            "V": 5,
            "X": 10,
            "L": 50,
            "C": 100,
            "D": 500,
            "M": 1000
        }
        total = 0
        for i in range(len(s) - 1):
            if roman[s[i]] < roman[s[i+1]]:
                total -= roman[s[i]]
            else:
                total += roman[s[i]]
        return total + roman[s[-1]]

 Longest Common Prefix--------------------------------------------------------------------
    class Solution:
    def longestCommonPrefix(self, strs: List[str]) -> str:
        res = ""
        for a in zip(*strs):
            if len(set(a)) == 1: 
                res += a[0]
            else: 
                return res
        return res


Valid Palindrome------------------------------------------------------
  class Solution {
    public boolean isPalindrome(String s) {
        int start = 0;
        int last = s.length() - 1;
        while(start <= last) {
        	char currFirst = s.charAt(start);
        	char currLast = s.charAt(last);
        	if (!Character.isLetterOrDigit(currFirst )) {
        		start++;
        	} else if(!Character.isLetterOrDigit(currLast)) {
        		last--;
        	} else {
        		if (Character.toLowerCase(currFirst) != Character.toLowerCase(currLast)) {
        			return false;
        		}
        		start++;
        		last--;
        	}
        }
        return true;
    }
}

Valid Anagram----------------------------------------------------------------

class Solution {
public:
    bool isAnagram(string s, string t) {
        sort(s.begin(), s.end());
        sort(t.begin(), t.end());
        return s == t;
    }
};

Reverse Words in a String-------------------------------------------------------
class Solution {
    public String reverseWords(String s) {
        String[] str = s.trim().split("\\s+");
        String out = "";
        for (int i = str.length - 1; i > 0; i--) {
            out += str[i] + " ";
        }
        return out + str[0];
    }
}

Count and Say--------------------------------------------------------------
class Solution {
    public String reverseWords(String s) {
        String[] str = s.trim().split("\\s+");
        String out = "";
        for (int i = str.length - 1; i > 0; i--) {
            out += str[i] + " ";
        }
        return out + str[0];
    }
}
