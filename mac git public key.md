Permission denied (publickey).
fatal: Could not read from remote repository.

Please make sure you have the correct access rights and the repository exists.


등록되지 않은 기기에서 clone이나 push가 일어나면 인증문제가 발생하게 된답니다.
결과적으로 유저의 ssh가 등록되지 않아 접근권한이 없어서 나오는 문제에요.

1. public key 생성
- $ ssh-keygen -t rsa -C "git이메일을 여기에 써주세요."
- Git 비밀번호를 쳐주시게되면(아무 비밀번호를 쳐도 됩니다.)

2. public key 복사
- 생성된 /Users/~~~/id_rsa.pub을 복사해줍니다.
- $ cat /Users/~~~/id_rsa.pub 안되면 
  $ cat ~/.ssh/id_rsa.pub
  ssh-rsa부터 그 시퀀스를 복사한다. 시퀀스 마지막에 자기 이메일이 보일텐데, 그 이메일도 포함하도록 끝까지 복사해주세요

3. github 에 settings
- 내 git의 settings 에 설정
  Settings >> SSH and GPG keys >> New SSH key
- Add SSH key



출처: https://zeddios.tistory.com/120