# Learning Regular Expressions

## TIP: A good regular expression should match the text you want to target and only that text, nothing more.

## website for practice
[https://regexr.com](https://regexr.com/)

[https://regex101.com](https://regex101.com/)

[https://regexpal.com](https://regexpal.com/)

# .(dot) 
- . 은 new line을 제외한 모든 글자를 나타냄
- /h.t/ : hat, hot, hit (heat은 안됨)
- \ : 다음글자를 escape시킴 (escape란 다음 글자를 metacharcters가 아닌 literal 글자로 인식하게함)
- /\./ : .을 literal로 인식하게함

# character set metacharacters
- \[ 와 \] 안에 들어있는 set (예: [0-9], [A-Z] 등)
- 여러개의 글자중에 한 오직 한개의 글자
- 글자set에 있는 글자들의 순서는 중요하지 않음
- /[aeiou]/ 는 모음중 한개의 글자를 나타냄
- /gr[ea]y/ 는 grey와 gray를 찾음
- /gr[ea]t/ 는 great를 못찾음(왜나면 []안에 한글자만 선택되기때문)


### Character Ranges
/[0123456789]/
/[abcdefghijklmnopqrstuvwxyz]/
/[ABCDEFGHIJKLMNOPQRSTUVWXYZ]/


### -(하이픈)으로 range를 나타낼 수 있음 
- 하이픈이 [] 안에 있을때만 range로 나타내고 []가 없으면 그냥 literal character로 - 임
- [0-9]
- [A-Za-z]
- 두자리 숫자 찾기 : [0-9][0-9]
- 세자리 숫자 찾기 :  [0-9][0-9][0-9]
- 전화번호의 형태 다 찾기(111-222-3333) : [0-9][0-9][0-9]-[0-9][0-9][0-9]-[0-9][0-9][0-9][0-9]
- 주의
  - [50-99] : 50~99까지의 숫자를 나타내지 않음!!!(한글자만 찾기때문이다!!)

# Negative Metacharacters
- ^ : negative 캐릭터 셋
- negative이란
  -- 여러개의 글자중 아무것도 아니어야함
  -- character set맨앞에 ^를 추가하면됨 --> 그럼 전체 character set을 negative set으로 바꿈
  -- /[^aeiou]/ #모음빼고 다 찾음(숫자,띄어쓰기,특수문자등도 다 찾음)
 - 주의
   - /see[^mn]/ # "see"는 못찾음. see뒤에 뭔가 하나 더 있어야함 "see." 이나 "see "는 찾음**
