# New-Year-s-Colorful-Celebrations

As the world welcomes Happy New Year 2026, a grand celebration street is decorated with a long strip of colorful lights. Each light glows in one of three festive colors:
R representing Red
G representing Green
B representing Blue
The lights are arranged in a row, forming a string s of length n.
A celebration segment is considered perfectly colorful if it contains all three colors Red, Green, and Blue at least once.
Your task is to count the number of substrings of the string that form a perfectly colorful celebration.

Input
The first line contains a single integer n, the length of the string.
The second line contains a string s of length n, consisting only of the characters 'R', 'G', and 'B'.
Output
Print a single integer, the number of substrings that contain all three characters 'R', 'G', and 'B'.

Constraints

1≤n≤10 
s[i]∈R,G,B

n = int(input())
s = input().strip()

count = {'R': 0, 'G': 0, 'B': 0}
l = 0
ans = 0

for r in range(n):
    count[s[r]] += 1

    while count['R'] > 0 and count['G'] > 0 and count['B'] > 0:
        ans += (n - r)
        count[s[l]] -= 1
        l += 1

print(ans)
