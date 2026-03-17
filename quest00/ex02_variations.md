# Palindrome Variations

## Python

    def palindrome(word):
    # Keep only letters and convert to lowercase
    clean = ''.join(char for char in word if char.isalpha()).lower()

    # A palindrome needs at least 3 characters
    if len(clean) < 3:
        return False

    # Start from both ends
    left = 0
    right = len(clean) - 1

    # Move inward until the pointers meet
    while left < right:
        # If the characters don't match, return the position
        if clean[left] != clean[right]:
            return (left, right)
        left += 1
        right -= 1

    # All characters matched
    return True

## Reflection

   I didn't miss anything, I just doublechecked the code I modified for checking if it's 2 or less characters. My original algorithm and code already took care of spaces, case-insensitivity and punctuation characters. I could also choose not to clean the string from everything but letters but since I'm not required to return the whole string back changed in any way nor do I actually change the original string through this function, I just stuck to it as I original thought to do it.
