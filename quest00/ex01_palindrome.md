# Palindrome

## Palindrome Alorithm

ALGORITHM palindrome(word):  
  
  //clean the string from anything different from letters  
  SET clean = keep_only_letters(word)  
  //make all characters lowercase so it's easier to compare  
  SET clean = convert_to_lowercase(clean)  
  
  // Compare from both ends  
  SET left  = 0  
  SET right = length(clean) - 1  
  
  WHILE left < right:  
  //because at all times left would be smaller and right larger  
   IF clean[left] != clean[right]:  
      //if at any point, the letters we check aren't equal, it's not a palindrome  
      RETURN FALSE  

   //advance the index position of left by one forward and right by one backward so they keep moving until they meet  
   left  <- left + 1  
    right <- right - 1  
  //if the loop continues without triggering the "RETURN FALSE", it has to be true  
  RETURN TRUE  
  
## Python Palindrome Function
  
  def palindrome(word):
    clean = ''.join(char for char in word if char.isalpha()).lower()

    left = 0
    right = len(clean) - 1

    while left < right:
        if clean[left] != clean[right]:
            return False
        left += 1
        right -= 1

    return True
  
## Reflection
  
  I missed one edge case where the string is a single space or letter. I should think beforehand to treat single or two letter strings as a non-palindrome and exclude them.  
  I would be able to write similar code using some language I know, not python or anything I only just used once. For new languages, I would need a bit  more time with trial and error but I'd get up to speed not before long.  
