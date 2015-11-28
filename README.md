<!DOCTYPE html>
<html>
	<head>
		<meta charset="utf-8">
		<title>Login Form</title>
		<script src="http://code.jquery.com/jquery-1.10.2.js"></script>
	</head>
	<body align=center>
		<form>
			Username: <input type="text" name="username" id="username"></input><br>
			Password: <input type="password" name="pw" id="pw"> </input><br>
			Country: <input type="text" name="country" id="country"></input><br>
			Age: <input type="number" name="age" id="age"></input><br>
			<button onclick="getValuesFromData();">Test</button>
		
		</form>
		<script>
			var username = document.getElementById('username').value;
			var password = document.getElementById('pw').value;
			var country = document.getElementById('country').value;
			var age = document.getElementById('age').value;
			function getValuesFromData(){
			$.post( "pageb.php", { username: username, password: password, country: country, age: age })
			.done(function( data ) {
			alert( "Data Loaded: " + data );
			
			
		});
		</script>
		<script>alert(document.getElementById('username').value);</script>
		
		
	</body>
</html>
