def palindrome(word):
    clean = ''.join(char for char in word if char.isalpha())

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


    ---Reflection---
    I didn't miss anything, I just doublechecked the code I modified for checking if it's 3 or less characters and remove the part that makes them all lowercase. I could also not clean the string from everything but letters but since I'm not required to return the whole string, I just stuck to it as I original thought to do it.