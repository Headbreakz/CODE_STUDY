## SQL 실행 순서

FROM  - WHERE - GROUP BY - HAVING - SELECT - ORDER BY



1. FROM
   * 전체 테이블 결과 값을 가져온다
2. WHREE
   * FROM절에서 읽어본 테이블에서 조건에 맞는 결과만 출력
3. GROUP BY
   * WHERE에서 간추린 데이터를 선택한 칼럼으로 작업
4. HAVING
   * GROUP BY 이후 사용되는 조건
5. SELECT
   * 조건 처리 이후 어떤 열을 출력할 것인지 선택
6. ORDER BY
   * 행의 순서





## SQL 문법

1. FROM
   * FROM 테이블명
2. WHERE
   * WHERE 조건
     * WHERE A = 2 	#A가 2인 경우만
     * WHERE A<>2    #A가 2가 아닌 경우
     * WHERE A ='2'   #A가 문자2인 경우
     * WHERE A IN NULL  #A가 NULL 경우만
     * AND
     * OR
     * NOT
   * 패턴 매칭
     * WHERE A LIKE 'HELLO%'      #A에서 HELLO로 시작하는 내용 경우
     * WHERE A LIKE '%HELLO%'   #A에서 HELLO가 포함된 내용이 있는 경우
     * WHERE A LIKE '%\\_%'            #A에서 _ 찾을 경우 \ 을 포함해야함 
3. ORDER BY
   * ORDER BY ASC    오름차순이 기본
   * ORDER BY DESC  내림차순
   * ORDER BY A ASC, B DESC  #A 오름차순하고, B 내림차순으로 정렬
4. LIMIT // MYSQL에서 사용
   * ORDER BY A DESC LIMIT 100   #내림차순으로 100개 행 출력
5. OFFSET
   * LIMIT 시작점
   * ORDER BY A DESC LIMIT 100 OFFSET 50 #50번 이후 51번부터 100개 행
6. SELECT
   * ALIAS
     * SELECT A*B AS C FROM *   #A와B를 곱한 결과가 C라는 새로운 별명