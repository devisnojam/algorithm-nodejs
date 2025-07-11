### 코딩 전

문제와 주어진 input / output 을 보고 영어 문장에서 공백으로 구분 된 단어의 개수만 세면 되는 문제로 이해했다.
만약 주어진 문자열이 " The first character is a blank " 처럼 공백이 앞 뒤로 있을 수 있기에
최악의 경우라도 반복문 횟수는 O(N) 이 된다고 생각했다.
문장 길이만큼 반복을 하면서 공백 횟수를 카운팅 하되
맨 앞이 공백이면 카운팅 하지 않고,
반복 횟수가 문자열 길이와 동일한데 공백이면 맨 마지막으로 보고 카운팅 하지 않도록
계획했다.

### 코딩 제출 후

계획한 대로 풀어서 제출했는데 틀렸다고 나오길래
질문게시판에서 다른 input 케이스를 찾아봤다.
내가 놓친 input 케이스로는

- "" -> 0
- " " -> 0
  정도가 있었다.

그래서 주어진 문자열에 앞 뒤 공백을 제거하기 위해 trim() 을 사용하여
그 결과가 빈 문자열이면 0으로 처리하고, 0이 아니면 정규식으로 공백 기준으로
split 처리해 개수를 반환하도록 생각했다.

### 다시 작성 제출 후

통과되었고, 다른 사람들 정답을 봐도 비슷했다.
이번 문제는 자료구조를 사용한 처리보다는
문제에 주어진 엣지케이스를 파악하고 코드에 적용할 수 있는지를
확인하려는 문제로 보였다.
