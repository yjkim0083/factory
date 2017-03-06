# redmine 설치 및 기본 설정

### redmine 설치
- redmine 설치파일 다운로드
    `$ wget https://bitnami.com/redirect/to/143427/bitnami-redmine-3.3.2-2-linux-x64-installer.run`

### redmine 경로
- /opt/redmine-3.3.2-2
- /opt/redmine-3.3.2-2/ctlscript.sh **start|stop|restart|status**

### redmine 계정
- 관리자 : admin / helloredmine

### redmine web
- http://192.168.0.165:8000/redmine

### redmine theme
- 경로 : /opt/redmine-3.3.2-2/apps/redmine/htdocs/public/themes
- 위의 경로 아래 다운로드 받은 테마관련 파일을 압축 해제 하여 저장한다.
- 관리 > 설정 > 표시방식 > 테마 에서 해당 테마를 선택 후 저장
