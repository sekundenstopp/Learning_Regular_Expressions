# Learning_Regular_Expressions

## website for practice
[https://regexr.com](https://regexr.com/)

[https://regex101.com](https://regex101.com/)

[https://regexpal.com](https://regexpal.com/)

---
## TIP: A good regular expression should match the text you want to target and only that text, nothing more.

---

# .(dot) 
. # new line을 제외한 모든 글자를 나타냄

/h.t/ = hat, hot, hit (heat은 안됨)

\   # 다음글자를 escape시킴 (escape란 다음 글자를 metacharcters가 아닌 literal 글자로 인식하게함)

/\./ # .을 literal로 인식하게함

# character set metacharcters
\[ # character set의 시작

\] # character set의 끝

 - 여러개의 글자중에 한 오직 한개의 글자
 - 글자set에 있는 글자들의 순서는 중요하지 않음
 - /[aeiou]/ 는 모음중 한개의 글자를 나타냄
 - /gr[ea]y/ 는 grey와 gray를 찾음
 - /gr[ea]t/ 는 great를 못찾음(왜나면 []안에 한글자만 선택되기때문)


### Character Ranges
/[0123456789]/
/[abcdefghijklmnopqrstuvwxyz]/
/[ABCDEFGHIJKLMNOPQRSTUVWXYZ]/
