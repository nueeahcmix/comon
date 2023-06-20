# COM:ON 프로젝트 (http://com0n.com/)
### Docker 컨테이너 및 이미지 기술을 통해 각 애플리케이션이 격리된 환경에서 실행되는 웹애플리케이션 스토어

<div align=center>
  <h3>Back-end</h3>
  <hr />
  <img src="https://img.shields.io/badge/SpringBoot-6DB33F?style=flat-square&logo=Spring Boot&logoColor=white"/>
  <img src="https://img.shields.io/badge/SpringSecurity-6DB33F?style=flat-square&logo=SpringSecurity&logoColor=white"/>
  <img src="https://img.shields.io/badge/MySQL-4479A1?style=flat-square&logo=MySQL&logoColor=white"/>
</div>
<div align=center>
  <h3>Front-end</h3>
  <hr />
  <img src="https://img.shields.io/badge/CSS3-1572B6?style=flat-square&logo=CSS3&logoColor=white"/>
  <img src="https://img.shields.io/badge/React-61DAFB?style=flat-square&logo=React&logoColor=white"/>
  <img src="https://img.shields.io/badge/Axios-5A29E4?style=flat-square&logo=Axios&logoColor=white"/>
</div>
<div align=center>
  <h3>etc</h3>
  <hr />
  <img src="https://img.shields.io/badge/docker-2496ED?style=flat-square&logo=docker&logoColor=white"/>
  <img src="https://img.shields.io/badge/amazonaws-232F3E?style=flat-square&logo=amazonaws&logoColor=white"/>
</div>

<div>
  <h3>Spring Security & JWT를 사용한 인증 처리 및 소셜 로그인</h3>
  <ul>
    <li>사용자의 이름, 이메일, 권한 정보 등을 포함한 토큰 생성</li>
    <li>BCryptPasswordEncoder를 사용한 비밀번호 암호화</li>
    <li>로그인 여부에 따른 접속 권한 처리 및 권한에 따른 페이지 접속 제한</li>
    <li>Naver Login API, Kakao Login API를 사용한 소셜 로그인</li>
  </ul>
</div>

<div>
  <h3>앱 스토어 기능 구현</h3>
  <ul>
    <li>개발자의 앱 등록 및 관리자의 심사</li>
      <ul>
        <li>MultipartFile을 통해 사진, 실행 파일(docker compose 스택을 만들기 위한 yaml 파일) 첨부</li>
        <li>I/O 입출력을 통한 실행 파일 다운로드 기능</li>
      </ul>
    <li>사용자 앱 다운로드 및 실행</li>
      <ul>
        <li>yaml 클래스를 사용한 사용자 고유 yaml 파일 생성</li>
        <li>독립적인 컨테이너 생성을 위한 포트 할당</li>
        <li>runtime.exec 메서드를 활용한 외부 프로세스 실행</li>
      </ul>
    <li>사용자 앱 리뷰 작성 및 통계</li>
    <li>관리자 페이지 통계 기능 구현</li>
      <ul>
        <li>HiChart 라이브러리를 사용한 차트 출력</li>
      </ul>
    <li>개인 정보 수정 및 탈퇴</li>
  </ul>
</div>

## 홈페이지 메인 공지사항 게시판

### 데이터베이스 연동 설정
- application.properties
- DatabaseConfiguration.java

### 게시판 목록 조회 기능
- NoticeApiController.selectNoticeList()
- NoticeService.selectNoticeList()
- NoticeServiceImpl.selectNoticeList()
- NoticeMapper.selectNoticeList()

### 게시판 목록 페이징 기능
- NoticeService.selectNoticeListCount()
- NoticeService.selectNoticeListPage(int offset)
- NoticeServiceImpl.selectNoticeListCount()
- NoticeServiceImpl.selectNoticeListPage(int offset)
- NoticeMapper.selectNoticeListCount()
- NoticeMapper.selectNoticeListPage(int offset)

### 게시판 카테고리 목록 조회 기능
- NoticeApiController.selectNoticeList(
			@RequestParam(value = "currentPage", required = false, defaultValue = "1") int currentPage)
- NoticeService.selectCategory()
- NoticeServiceImpl.selectCategory()
- NoticeMapper.selectCategory()

### 게시판 카테고리별 게시글 출력 기능
- NoticeApiController.selectCategoryList()
- NoticeService.selectCategoryList(int noticeCategoryIdx)
- NoticeServiceImpl.selectCategoryList(int noticeCategoryIdx)
- NoticeMapper.selectCategoryList(int noticeCategoryIdx)

### 게시판 상세 조회 기능
- NoticeApiController.selectNoticeDetail()
- NoticeService.selectNoticeDetail(int noticeIdx)
- NoticeServiceImpl.selectNoticeDetail(int noticeIdx)
- NoticeMapper.selectNoticeDetail(int noticeIdx)

### 게시판 등록 기능
- NoticeApiController.writeNotice()
- NoticeService.writeNotice(NoticeDto noticeDto)
- NoticeServiceImpl.writeNotice(NoticeDto noticeDto)
- NoticeMapper.writeNotice(NoticeDto noticeDto)

### 게시판 수정 기능
- NoticeApiController.updateNotice()
- NoticeService.updateNotice(NoticeDto noticeDto)
- NoticeServiceImpl.updateNotice(NoticeDto noticeDto)
- NoticeMapper.updateNotice(NoticeDto noticeDto)

### 게시판 삭제 기능
- NoticeApiController.deleteNotice()
- NoticeService.deleteNotice(int noticeIdx)
- NoticeServiceImpl.deleteNotice(int noticeIdx)
- NoticeMapper.deleteNotice(int noticeIdx)
 
### 메인 footer에 노출될 게시물
- NoticeApiController.selectNoticeForFooter()
- NoticeService.selectNoticeForFooter()
- NoticeServiceImpl.selectNoticeForFooter()
- NoticeMapper.selectNoticeForFooter()

### 로깅 기능 구현

### 인터셉터를 이용한 요청 시작과 끝 로그 출력

### AOP를 이용한 Controller, ServiceImpl, Mapper 로그 출력

### @Transactional 어노테이션을 이용한 트랜잭션 설정

### AOP를 이용한 트랜잭션 설정

<div>
  <h3>샘플 앱 9개 제작</h3>
  <ul>
    <li>Habit-tracker</li>
      <ul>
        <li>습관 체크 기능 및 월간 전체 통계 차트</li>  
        <li>HiChart 라이브러리를 사용한 차트 출력</li>  
      </ul>
    <li>연봉 연차 계산기</li>
      <ul>
        <li>입사일을 사용해 연차 개수, 근무 일수 계산</li>  
        <li>사람인 API를 사용해 연봉 및 연차 계산</li>
      </ul>
    <li>comPlace</li>
      <ul>
        <li>키워드 검색을 통한 장소 검색</li>  
        <li>KakaoMap API를 사용한 지도 기능 구현</li>
      </ul>
    <li>Logon</li>
       <ul>
        <li>월별 일기장 작성 기능</li>  
        <li>FullCalendar 라이브러리를 사용한 달력 기능 구현</li>  
      </ul>
    <li>테트리스</li>
       <ul>
        <li>테트리스 게임</li>
        <li>오픈 소스를 기반으로 한 테트리스 게임 구현</li>
        <li>프론트엔드: <a>https://github.com/nueeahcmix/tetris-react.git</a></li>
      </ul>
    <li>슬기로운 회사 생활</li>
       <ul>
        <li>백과사전</li>  
        <li>Naver Open API를 사용한 사전 기능 구현</li>  
        <li>백엔드: <a>https://github.com/nueeahcmix/dictionary.git</a></li>
        <li>프론트엔드: <a>https://github.com/nueeahcmix/dictionary-react.git</a></li>
      </ul>
    <li>COM:ONEWS</li>
       <ul>
        <li>관심 분야 뉴스 검색(크롤링)</li>  
        <li>Naver Open API를 사용한 크롤링 기능 구현</li>  
        <li>프론트엔드: <a>https://github.com/nueeahcmix/news-react.git</a></li>
      </ul>
    <li>Onday Schedule</li>
       <ul>
        <li>일정 관리 앱 </li>  
        <li>FullCalendar 라이브러리 및 Google Calendar API를 사용한 기능 구현</li>
      </ul>
    <li>맞춤법 검사기</li>
       <ul>
        <li>맞춤법 검사기 앱</li>  
        <li>부산대 맞춤법 검사기 API를 사용한 기능 구현</li>  
      </ul>
  </ul>
</div>
