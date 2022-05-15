# sparta_web-basic
[스파르타코딩클럽] 웹개발 종합반

업데이트 파일 : index.html 파일 업데이트 되었습니다.

목표 : 영화 웹 피디아 홈페이지 제작하기.

내용 : 
88~102 번 코드 업데이트
ajax를 사용하여 GET타입으로 미세먼지정보를 realtime으로 불러와서
JSON 타입의 데이터에서
딕셔너리 안에 있는 구 정보와 미세먼지 농도 정보를 받아와 출력합니다
예) 강남구 156

            success: function (response) {
                let rows = response['RealtimeCityAir']['row']

                for (let i = 0; i <rows.length; i++) {   //반복문을 통해서 'row' 딕셔너리 안의 정보를 훑어봅니다. 
                    let gu_name = rows[i]['MSRSTE_NM']   //지역 이름을 받아 gu_name이라는 변수에 담아둡니다.
                    let gu_mise = rows[i]['IDEX_MVL']    //미세먼지 농도를 받아 gu_mise라는 변수에 담아둡니다.
                    console.log(gu_name, gu_mise)
                }

