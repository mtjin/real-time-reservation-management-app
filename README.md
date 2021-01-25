

# 안드로이드 인턴 회의실 실시간 예약관리 앱 인턴 프로젝트 (2020.07-2020.08) (3주 설계, 3주 개발-테스트-PPT 발표준비 진행) (개인)


## 실시간으로 회의실이 예약관리 되는 회의실 앞에 배치될 태블릿 앱과 사용자 스마트폰 앱 두 종류의 앱 개발
---

**1) URL**

설명 : https://www.notion.so/717aec3c3cbc4406803c39c050e92694

시연 영상 : [https://www.youtube.com/watch?v=RAQpGx08eSw&feature=youtu.be](https://www.youtube.com/watch?v=RAQpGx08eSw&feature=youtu.be)

**2) 설명**

- 인턴 2개월 동안 개인 프로젝트 과제를 부여받아 설계부터(요구사항명세서, 유스케이스, 화면설계, 시퀀스다이어그램, 개발설계) 개발 및 테스트까지의 현업 프로세스를 경험
- 사용자의 모바일 앱과 회의실 앞의 태블릿 앱을 파이어베이스의 Real Time Database를 통해 동기화하여 실시간 회의실 예약 관리하는 2개의 앱 개발
- WorkManager 와 AlarmManager 를 사용해 회의시작 15분전 알림 구현
- 태블릿 앱에서 예약 1~3 단계 비슷한 UI에 공유할 데이터가 많아 SharedViewModel 적용
- [Git Flow 적용] 브랜치  전략 :  master → 출시단계, develop → 개발단계, feature/기능명 → 기능 구현 총 3단계로 브랜치 적용, feature 의 경우 구현해야할 기능을 Issue로 남기고 그에 맞는 이슈와 기능명으로 명명
- Jetpack Navigation 을 사용하여 Single Page Application 구조, 태블릿 앱은 화면이 크다는 특징을 활용하여 상단, 하단 멀티 네비게이션 구조 적용
- DI Graph 설계 및 Dagger2 로 의존성 주입
- RxJava PublishSubject를 활용한 자동검색 기능 구현
- 예약 시간 예외처리 및 타임스탬프 관리
- Mockito, Junit4, Espresso 로 Unit Test 및 Jacoco 로 Test Coverage 확인
- 파이어베이스가 느리다는 단점을 보완하기 위해 로컬 캐싱 적용 (RxJava concat)
- 익명, 로그인, QR 코드 예약 같은 다양한 회의실 예약방법 제공
- MediaStore API 사용으로 안드로이드 11 Scoped Storage 대응 및 구글의 지침대로 런타임 권한 획득 지향

**3) 기술 스택**

 Android(Kotlin), Dagger2, WorkManager, AlarmManager, Jetpack Navigation,
MVVM, AAC ViewModel, LiveData, Databinding, Retrofit2, Room, RxJava2, RxAndroid, Unit Test(Mockito, Junit4, Espresso), Glide, Firebase(Authentication, FCM, RTDB, Storage), Timber, Material Desgin, Zxing QR Code 등

**4) 성과**

설계부터 개발 및 테스트 까지의 프로세스와 안드로이드 현업 경험

태블릿앱 30개, 사용자앱 25개 유닛테스트 완료

Dagger2 그래프 설계 및 구현 

Git Flow 적용

소나큐브와 코드리뷰를 통한 클린코드 지향

태블릿앱 개발 경험


**5) 아키텍처**


<img src="https://user-images.githubusercontent.com/37071007/105709449-0ffe8a80-5f59-11eb-96eb-02c6a078bd88.png" align="left">

<img src="https://user-images.githubusercontent.com/37071007/105709464-17be2f00-5f59-11eb-827f-8c8ce2c74bac.png" align="left">

<img src="https://user-images.githubusercontent.com/37071007/105709502-2573b480-5f59-11eb-8bc7-17619004fa3f.png" align="left">

<img src="https://user-images.githubusercontent.com/37071007/105709518-2b699580-5f59-11eb-8699-fc62539e6832.png" align="left">
