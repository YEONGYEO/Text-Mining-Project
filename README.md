# Text Mining Project   
문서 수집 (crawling) > 형태소 분석 (koNLPy) > 시각화 (web, spring-boot, wordcloud, amcharts)
- Developent enviroment setting

> python 3.x ver    
> database - elasticsearch, mysql   
> web - spring boot 2.x ver with mybatis, maven, thymeleaf, AM chart   
   
- functions (python 3.x)
> crawiling naver news   
> data preprocessing    
> calculate tf (term frequency)   
> calculate ngram (related search terms)  
   
***
### naver news crawler
this is using Korean   
- BuautifulSoup - bs4 and selenium   
- upload 4 version of crawling code   
> korean window os   
> korean linux os   
> english window os   
> english linux os   

***
### python project
총 10개의 파일  
실제 테스트를 위해서는 ex.py, mysql.py 에서 host, port, user, passwd, db 등 정보 입력해야 함   

|파일|설명|
|------|---|
|[main.py](https://github.com/YEONGYEO/Text-Mining-Project/blob/master/project/main.py)|project 전체 main 함수 실행 시, 모든 코드 실행|
|[crawler.py](https://github.com/YEONGYEO/Text-Mining-Project/blob/master/project/crawler.py)|네이버 뉴스 크롤링 기능|
|[data_preprocessing.py](https://github.com/YEONGYEO/Text-Mining-Project/blob/master/project/data_preprocessing.py)|형태소 분석, 명사 추출, 불용어 처리 등 데이터 정제|
|[es.py](https://github.com/YEONGYEO/Text-Mining-Project/blob/master/project/es.py)|elasticsearch 저장 및 검색|
|[df_export.py](https://github.com/YEONGYEO/Text-Mining-Project/blob/master/project/df_export.py)|dataframe export to csv, excel, txt|
|[mysql.py](https://github.com/YEONGYEO/Text-Mining-Project/blob/master/project/mysql.py)|mysql 저장 및 검색|
|[ngram.py](https://github.com/YEONGYEO/Text-Mining-Project/blob/master/project/ngram.py)|연관검색어 기능 구현|
|[tfidf.py](https://github.com/YEONGYEO/Text-Mining-Project/blob/master/project/tfidf.py)|단어 빈도수 계산, sklearn tfidf 행렬 값 계산|
|[stop.txt](https://github.com/YEONGYEO/Text-Mining-Project/blob/master/project/stop.txt)|불용어 text file|

   
- 전체 과정
![function process](./images/python_process.PNG)      
- MySql database 구조
![DB structure](./images/mysql_db.PNG)
   

***
### web   
> spring boot 2.x ver with mybatis, maven, Thymeleaf, Bootstrap, AM charts 4    
   
- AM charts 4
> [Force-directed network](https://www.amcharts.com/demos/force-directed-network/)   
> [Changing data of Word cloud](https://www.amcharts.com/demos/changing-data-word-cloud/)   
> [Clustered Bar Chart](https://www.amcharts.com/demos/clustered-bar-chart/)     
    
- spring boot 구조   
지금 현재 프로젝트에는 2가지 방식의 구조가 있음   
mapper에서 가져온 데이터는 controlelr가 view 한테 보내고 다시 view를 가져와서 client 에 응답   
   
   - client > controller > service > service implement > dao > mapper xml > db
   - client > controller > mapper > mapper xml > db
   
- 시연 동영상   
주제 : 2020 도쿄 올림픽   
   
[![web testing](https://img.youtube.com/vi/fTSoUUpPoDI/maxresdefault.jpg)](https://www.youtube.com/watch?v=fTSoUUpPoDI?t=0s)


