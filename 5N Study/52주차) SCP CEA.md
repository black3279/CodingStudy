## 2023년04 23
SCP CEA 공부법 추천
1줄요약 : AWS SAA의 SDS 버전            https://subbak2.com/114

공부법 추천
1) 패스트 트랙 (AWS SAA 먼저 공부, 또는 T3 교육 이수)
 ① scp 홈페이지 가서 "서비스 소개", "아키텍처 센터" 페이지를 본다
https://cloud.samsungsds.com/serviceportal/index.html

 ② SCP Hands-on 컨플루언스(SDS VDI에서 접속 가능)에서 Console 사용법을 본다
auto scaling 구성 순서 맞추기

2) 기초부터 하고 싶은 사람 ( 약 38시간 )
 ① 동영상 강의를 듣는다        https://lc.multicampus.com/cloud-academy/
     → 안드로이드, iOS 모바일 앱도 가능. 총 시간 약 30시간

 ② SCP Hands-on 컨플루언스(SDS VDI에서 접속 가능)에서 Console 사용법을 본다

3월 회고 (Trouble shooting)https://subbak2.com/191

  
DROP TABLE PURGE 테이블 복구 https://subbak2.tistory.com/190
PK 채번과 시퀀스
 1) 시퀀스 옵션에 담긴 의미 - https://subbak2.tistory.com/16
 2) DBA가 발견하고 해결해야할 기술부채 - 3. 시퀀스 최댓값 https://subbak2.tistory.com/125


Amazon RDS for Oraclehttps://subbak2.com/124+ AWS 아키텍트 강의
1) spec에 명시되어있지는 않지만 Volume * 4의 IOPS가 가능하다
2) RDS도 EC2 위에 설치한 서버다
재부팅시 IP가 바뀌는 이유
OS패치시 DownTime이 발생하는 이유
3) 서비스 특성에 따라 SE2라는 선택지 가능
4) RAC가 되는 버전이 출시됨 (비공식)
5) WAS가 Multi AZ인 경우 성능 지연 가능
