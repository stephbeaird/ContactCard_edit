# ContactCard_edit<!DOCTYPE html>
<html lang="en">
	<head>
		<meta charset="UTF-8">
		<title>Contact Card</title>
		<link rel="stylesheet" type="text/css" href="styles.css">
		<script type="text/javascript" src="https://code.jquery.com/jquery-3.2.1.js"></script>
		<script type="text/javascript">
			$(document).ready(function(){
				$("button").click(function(){

				var first = $("#first").val();
				var last = $("#last").val();
				var desc = $("textarea").val();

				$('#left').append("<div id= 'card'><p>" + first + " " + last +"</p><p id= 'back'> " + desc +"</p></div>");


				$("#first").val("");
				$("#last").val("");
				$("#desc").val("");	

				return false;

				});

				$(document).on('click', '#left', function(){
					$(this).children();
				});
			});
		</script>
	</head>
	<body>
		<div class="wrapper">
			<div id="left">
				<form>
					<br><br>
					<label for="first">First name:</label>
					<input type="text" placeholder="First Name" name="FirstName" id="first">
					<br><br>
					<label for="last">Last name:</label>
					<input type="text" placeholder="Last Name" name="LastName" id="last">
					<br><br>
					<textarea for="desc"></textarea>
					<input id="Description">
				</form>
				<button id="btn">Add User</button>
			</div>
		</div>
	</body>
</html>
