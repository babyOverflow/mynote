# pam - Pluggable Authentication Modules for Linux

## DESCRIPTION
Linux-PAM은 응용프로그램의 인증 처리를 다루는 라이브러리를 위한 시스템이다.

PAM의 주요 특징은 인증은 동적으로 구성할 수 있다는 것입니다. 다른말로 시스템 관리자는 개별 이 프로그램이 어떻게 유저를 확인할 지 선택할 수 있습니다. 설정 파일은 `/etc/pam.conf`에 위치합니다. 다른 방법으로 `/etc/pam.d/` 디렉토리에 설정 파일들이 있을 수 있습니다. 만약 `pam.d` 디렉토리가 존재한다면 `pam.conf`를 무시합니다.

벤더가 제공하는 pam 설정은 `/usr/lib/pam.d/` 디렉토리에 위치합니다. `/etc/pam.d/`의 설정이  `/usr/lib/pam.d/`의 설정을 덮어쓰기 때문에  `/etc/pam.d/`의 설정의 우선순위가 높습니다. 


## FILES
/etc/pam.conf
	the configuration file
	
/etc/pam.d
	the Linux-PAM configuration director. Gennerally, if this is directory id present, the /etc/pam.conf file if ignored.
	
/usr/lib/pam.d
	the Linux-PAM vendor configuration directory. Files in /etc/pam.d oeverride files with the same name in this direnctory.

---
#pam_conf #pam_d #linux #born2beroot

man 7 pam

---
