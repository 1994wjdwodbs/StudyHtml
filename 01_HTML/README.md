# HTML 기본학습

## 웹 페이지 기본 구조와 작성 방법
태그, 요소, 속성의 의미 이해 및 HTML, CSS, JS 작성방법 따라하기

## HTML5 기본 태그
블라블라~~

## HTML5 입력 태그
```html
<!DOCTYPE html>
<html>
<head>
    <meta charset='utf-8'>
    <meta http-equiv='X-UA-Compatible' content='IE=edge'>
    <title>Page Title</title>
    <meta name='viewport' content='width=device-width, initial-scale=1'>
</head>
<body>
    <!-- 사용자 입력 양식 -->
    <form>
        <input type="text" name="txt_userid" value="personar95"><br>
        <input type="password" name="password" value="12345"><br>
        <input type="file" name="attach_file"><br>
        <input type="checkbox" name="chk_hobby_swim" value="SWIM">수영<br>
        <input type="checkbox" name="chk_hobby_marathon" value="MARATHON">마라톤<br>
        <input type="radio" name="rdo_gender" value="M">남자
        <input type="radio" name="rdo_gender" value="F">여자
        <input type="radio" name="rdo_gender" value="G">중성<br>

        <!--<input type="datetime" name="dt_today" value="2021-01-28 14:50:00"><br>-->
        
        <!-- 보이지 않는 양식 -->
        <input type="hidden" name="hdn_temp_val" value="25683252923"><br>
        <!-- 버튼 -->
        <input type="button" name="btn_normal" value="버튼"><br>
        <input type="reset" name="btn_reset" value="리셋"><br>
        <input type="submit" name="btn_submit" value="제출"><br>
        <!-- 기타 -->
        <input type="image" src="https://placehold.it/400x250"><br>

    </form>
    <!-- 사용자 입력 양식 -->
</body>
```
[이전](https://github.com/1994wjdwodbs/StudyHtml)
