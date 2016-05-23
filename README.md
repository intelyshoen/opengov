# 서울 정보소통광장 행정정보 공개
서울시는 결재문서, 정책연구보고서 등 시가 생산한 약 500만 건이상의 주요 행정정보 목록을 깃허브에 공개합니다. 이를통하여 서울시 공공데이터에 대한 접근성과 활용성을 높일 수 있을 것으로 기대합니다. 
> 원본데이터 : [서울정보소통광장](http://opengov.seoul.go.kr)

 
# 정보공개 대상
* **결재문서**
 * 서울시가 생산한 모든 결재문서와 원문공개 대상을 함께 제공
 * 대상 기관 : 서울시 본청(사업소 포함)
 * 공개 범위 : 2015년 1월 ~ 2016년 5월 현재(약1백만건)
 * 생성주기 : 매주 업데이트 , 매주 월요일 등록(전주,월~일까지)
 * 초기데이터
   * 2015.1월~2016년 4월, 월별 데이터생성 : 20150301_20150331_info_list.csv 
   * 2016.5월 이후, 주별 데이터 생성 : 20160509_20150515_info_list.csv 
* **정책연구보고서**
 * 12개 기관(서울시 및 산하 투자출연기관 등)의 정책보고서와 연구보고서 공개
 * 대상 기관 : 서울시(학술용역, 기술용역), SH도시연구원, 보건환경연구원, 서울디자인 재단, 서울물연구원, 서울시복지재단, 서울시립대 서울학연구소, 서울시여성가족재단, 서울연구원, 서울특별시의회, 한성백제박물관
 * 공개 범위 : 정보소통광장 서비스 대상 전체
 * 생성주기 : 매월 업데이트 , 매월 첫 업무일 등록 (전월, 휴일이 지난 첫 업무일)
 * 초기데이터
   * ~2016년 4월 , 일괄 데이터생성( 약17.268건) : 20150101_20160430_research_list(util 2016.04).csv (해당 데이터들의 최초 생산일 확인 필요) 
   * 2016.5월 이후, 2016년6월 1일 생성 
* **사전정보공표**
 * 시민이 정보공개를 청구하기 전에 미리 공개하는 행정정보 서비스로, 약 327종 513개 업무에 대한 정보를 공개하고 있음
 * 제공 범위 : 복지, 건강 등 12개 분야, 513개 공표업무
 * 공개 범위 : 정보소통광장 서비스 대상 전체
 * 생성주기 : 매월 업데이트 , 매월 첫 업무일 등록 (전월, 휴일이 지난 첫 업무일)
 * 초기데이터
   * ~2016년 4월, 일괄 데이터생성( 약6,355건) : 20150101_20160430_public_list.csv
   * 2016.5월 이후, 2016년6월 1일 생성 
 

# 데이터 이용 안내
### 디렉토리명 
 * 구성 : /분야명+'_'+종류  
 * 예시
  * 정보목록 : info_list
  * 사전정보공표목록  : public_list
  * 정책연구자료목록  : research_list
 
 
### 파일명          
 * 구성 : 기준년월일(from)+'_'+기준년월일(to)+'_'+분야명+종류+'_'+(필요시설명)+'.'+확장자
 * 예시
  * 정보목록 : 20150301_20150331_info_list.csv 
  * 사전정보공표목록 : 20150301_20150331_public_list.xml
  * 정책연구자료목록 : 20150301_20150331_research_list.xlsx
 
 
### 분야별 항목설명 (별도 표시 없는 경우 NOT NULL항목)
 * **정보목록**
  * package_id      : 문서관리번호(PK)
  * doc_prdctn_dt   : 자료생산일자
  * trck_card_nm    : 단위과제카드명
  * title           : 제목
  * src_dept_doc_id : 문서번호 (예: 정보공개정책과-1234)
  * writer          : 담당자
  * othnd_pd        : 문서보존기간
  * dept_nm         : 부서명
  * othbs_se        : 공개구분코드(공개,부분공개,비공개)
  * url             : 원문공개URL, *nullable*
 
 
 * **사전정보공표목록**
  * nid             : 관리번호(PK)
  * category        : 분야
  * title           : 제목
  * writer          : 담당자
  * dept_nm         : 부서명
  * regist_dt       : 등록일시(정보소통광장 등록일시)
  * taxonomy        : 업무상세분류
  * telno           : 전화번호, *nullable*
  * cpyrht          : 라이선스
  * url             : url
 
 
 * **정책연구자료목록**
  * nid             : 관리번호(PK)
  * title           : 제목
  * regist_dt       : 등록일시
  * relm_cl         : 자료유형
  * creat_yr        : 생산년도
  * category        : 분야
  * region          : 관련지역
  * isbn            : ISBN, *nullable*
  * relte_area      : 원본시스템
  * writer          : 담당자
  * doc_prdctn_dt   : 자료생산일자
  * cpyrht          : 라이선스
  * othbs_se        : 공개구분
  * job_se          : 작업구분
  * url             : url
 
 

