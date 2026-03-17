# Palindrome Variations

## Python

    def palindrome(word):
    clean = ''.join(char for char in word if char.isalpha()).lower()

    if len(clean) < 3:
        return False

    left = 0
    right = len(clean) - 1

    while left < right:
        if clean[left] != clean[right]:
            return (left, right)
        left += 1
        right -= 1

    return True

## Reflection

   I didn't miss anything, I just doublechecked the code I modified for checking if it's 2 or less characters. My original algorithm and code already took care of spaces, case-insensitivity and punctuation characters. I could also choose not to clean the string from everything but letters but since I'm not required to return the whole string back changed in any way nor do I actually change the original string through this function, I just stuck to it as I original thought to do it.
