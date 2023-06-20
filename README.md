# COM:ON 프로젝트 (http://com0n.com/)

## 홈페이지 공지사항 게시판

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

