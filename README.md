<html>
<script>
function aaa() {
	fir = new Array(45);
	sec = new Array(6);
	for (i = 0; i < 45; i++) fir[i] = i + 1;
	for (i = 0; i < 6; i++) {
		ran = parseInt(Math.random()*fir.length);
		sec[i] = fir[ran];
		fir.splice(ran,1);
		for (h = fir.length; h; h -= 1) {
			j = Math.floor(Math.random() * h);
			x = fir[h - 1];
			fir[h - 1] = fir[j];
			fir[j] = x;
		}
	}
	for (i = 0; i < 6; i++) {
		for (j = 0; j <= i; j++) {
			if(sec[i] <= sec[j]) {
				k = sec[i];
				sec[i] = sec[j];
				sec[j] = k;
			}
		}
	}
	document.getElementById('ddd').innerHTML = sec;
}
</script>
<h1> ♥빳대리 로또♥</h1>
<h2> 아수라 발발타, 박대리의 나와라 로또 번호 </h2>
<input id="button1" type="button" onclick="aaa()" value="CLICK!" style="width:300px;height:50px;font-size:30px;">
<br/><br/>
<div id="ddd" style="font-size:30px;border:1px solid;width:300px;height:50px;text-align:center;padding:10px;"></div>
	<br><br>
<h3> <경고> 위 번호로 당첨시, 세전 당첨금에서 수수료 40% 가 자동 차감됩니다</h3>
	<style>
		h3{
		color:red;
		}
	<br><br><br>
	<h1> 지금 롯데캐슬에 갇혀있나요, 인재여? </h1>
	<input id="night_day" type="button" value="집에 가고 싶을 때 누르는 버튼" onclick="
		if(document.querySelector('#night_day').value === '집에 가고 싶을 때 누르는 버튼'){
		document.querySelector('body').style.backgroundColor = 'black';
		document.querySelector('body').style.color = 'red';
		document.querySelector('#night_day').value = '안돼 못 가. 엑셀을 다시 켜라.';
		} else {
		document.querySelector('body').style.backgroundColor = 'white';
		document.querySelector('body').style.color = 'black';
		document.querySelector('#night_day').value = '집에 가고 싶을 때 누르는 버튼';
	}
		">
    <input id="샤따" type="button" value="다섯시가 넘었다면 클릭해도 좋다" onclick="
      if(document.querySelector('#샤따').value === '다섯시가 넘었다면 클릭해도 좋다'){
      document.querySelector('body').style.backgroundColor = 'yellow';
      document.querySelector('body').style.color = 'navy';
      document.querySelector('#샤따').value = '업무 샤따를 내려주세요';								     ';
      } else {
      document.querySelector('body').style.backgroundColor = 'white';
      document.querySelector('body').style.color = 'black';
      document.querySelector('#샤따').value = '다섯시가 넘었다면 클릭해도 좋다';
    }
      ">
</html>
