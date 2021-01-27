<%@ page language="java" contentType="text/html; charset=UTF-8"
    pageEncoding="UTF-8"%>
<!DOCTYPE html>
<html>
<head>
<meta charset="UTF-8">
<title>Insert title here</title>
<style type="text/css">
	.valid_info{
		color: red;
		font-size:0.5vw;
	}
</style>
</head>
<body>
<h1>회원 가입 양식</h1>
	<form action="${context}/member/joinimpl.do" method="post" id="frm_join">
		<table>
			<tr>
				<td>ID :</td>
				<td>
					<input type="text" name="id" id="id" size="10" required/>
					<span class="valid_info" id="idCheck"></span>
				</td>
			</tr>
			<tr>
				<td>PASSWORD :</td>
				<td>
					<input type="password" name="pw" id="pw" required/><br>
					<span class="valid_info" id="pw_confirm"></span>
				</td>
				
			</tr>
			<tr>
				<td>휴대폰번호 :</td>
				<td><input type="tel" name="tell" required/></td>
			</tr>
			<tr>
				<td>email :</td>
				<td><input type="email" name="email" required/></td>
			</tr>
			<tr>
				<td colspan="2" align="center">
				<input type="submit" value="가입" />
				<input type="reset" value="취소" />
				</td>
			</tr>
		</table>
	</form>
	<script type="text/javascript">
	// 아이디 체크를 했는지 확인하기위핸 flg
	let idCheckFlg = false;
	
		document.querySelector('#frm_join').addEventListener('submit',(e)=>{
			
			// 요소의 아이디로 엘리먼트 객체 호출 가능. (웹표준이 아님)
			let password = pw.value;
			let regExp = /^(?!.*[ㄱ-힣])(?=.*\W)(?=.*\d)(?=.*[a-zA-Z])(?=.{8,})/;
			// 정규표현식에 맞지 않는다면
			if(!(regExp.test(password))){
				//부합하지 않는다면 form에 데이터 전송을 막아주고
				e.preventDefault();
				// 경고문구 보내주기
				pw_confirm.innerHTML = '비밀번호는 숫자, 영문, 특수문자 조합의 8글자 이상이어야 합니다.'
				pw.value = "";
			}
		});
	</script>
</body>
</html>