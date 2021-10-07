VSCode, code-server // VSCode 웹에서 사용하기

참고주소 https://tong9433.github.io/blog/002#/

1) unix 계정
UNIX username : (사용자계정)
UNIX password : (사용자비밀번호)

2) Ubuntu 명령어
  $ sudo apt-get install build-essential net-tools
  $ wget -q https://github.com/cdr/code-server/releases/download/3.4.1/code-server_3.4.1_amd64.deb
  $ sudo dpkg -i code-server_3.4.1_amd64.deb
  $ echo "export PASSWORD='{비밀번호}'" >> ~/.bashrc # 접속 시 암호, 꼭 설정!
  $ source ~/.bashrc
  $ sudo ufw allow 포트번호/tcp # 포트번호의 port 방화벽 해제

3) 몇가지 패키지 설치
  $ code-server --install-extension ms-vscode.cpptools ms-vscode.cpptools formulahendry.terminal hookyqr.beautify
  $ code-server

4) http://localhost:(포트번호)

5) 포트포워딩 하기 (외부에서 사용하기 위함)
ifconfig
	입력후 inet address 내용 메모 (내부 IP주소)
code-server --bind-addr (내부IP주소):(포트번호)
	입력하여 사용할 내부포트 설정
