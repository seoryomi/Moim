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
<h1> ♥엠트리로또♥</h1>
<h2> 수리수리 마수리, 박대리의 나와라 로또 번호 </h2>
<input id="button1" type="button" onclick="aaa()" value="CLICK!" style="width:300px;height:50px;font-size:30px;">
<br/><br/>
<div id="ddd" style="font-size:30px;border:1px solid;width:300px;height:50px;text-align:center;padding:10px;"></div>
	<br><br><br><br><br>
<h1> 집에 가고 싶은가요, 휴먼? </h1>
	<input id="night_day" type="button" value="집에 가고 싶을 때 누르는 버튼" onclick="
		if(document.querySelector('#night_day').value === '집에 가고 싶을 때 누르는 버튼'){
		document.querySelector('body').style.backgroundColor = 'black';
		document.querySelector('body').style.color = 'red';
		document.querySelector('#night_day').value = '안돼 다시 돌아가';
		} else {
		document.querySelector('body').style.backgroundColor = 'white';
		document.querySelector('body').style.color = 'black';
		document.querySelector('#night_day').value = '집에 가고 싶을 때 누르는 버튼';
	}
		">
</html>
