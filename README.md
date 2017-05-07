### re-coloring-illustrator with json
--------

0. ai-scripts 설치
 + terminal 실행
 ```
 cd / 
 cd /Applications/Adobe\ Illustrator\ CC\ 2017
 cd Presets.localized/ko_KR/스크립트 (OS 언어에 따라 달라짐)
 git clone "https://github.com/newsdev/ai-scripts.git" 
 ```

1. Google Spreadsheet에서 서울시 구별 랜덤값 입력
 + [예제파일](https://goo.gl/DGg83S)
 + =RANDBETWEEN(0,500) 함수
 + 시트2번에 함수식 제외하고 값만 붙여넣기로 raw-data 완성
 + csv download

2. http://www.convertcsv.com/에서 csv to json 진행
 + csv file upload
 + output type은 두번째 CSV To Keyed JSON으로 변경

3. 다운로드 받은 json은 문서편집기에서 최종 정제
 + "FIELD4" -> "stroke"
 + "FILED5" -> "fill"
 + "FALSE" -> false (" " 제외)
 + 제일 바깥을 감싸는 배열 생성해주고
 + 한단계 아래 key는 아래 그림과 같이 해준다
 + ![image1](

 4. Illustrator 실행한 후 
  + ai scripts -> colorize artwork 실행
  + 제대로 값이 반영됐는지 확인
