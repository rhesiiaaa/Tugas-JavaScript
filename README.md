<!DOCTYPE html>
<html>
<head>
    <td>
        <img src="D:\SEMESTER 3\IntAppProjects\DSC01123.jpg" width="100px"
            style="display: block;border-radius: 50%;border-color:white;margin-right:30px" border="2px"></td>     
	<h2>Inputkan Nama dan Jumlah Pilihan</h2>
	<form>
		<label for="nama">Nama:</label><br>
		<input type="text" id="nama" name="nama"><br>
		<label for="jumlah_pilihan">Jumlah Pilihan:</label><br>
		<input type="number" id="jumlah_pilihan" name="jumlah_pilihan"><br><br>
		<input type="button" value="OK" onclick="generateText()">
	</form> 
	<div id="text-input"></div>
</head>
<body>
    <title>JavaScript</title>
	<script>
		function generateText() {
			var jml = document.getElementById("jumlah_pilihan").value;
			var textInput = "";
			for (var i = 1; i <= jml; i++) {
				textInput += "<label for='inputan" + i + "'>Pilihan " + i + ":</label><br>";
				textInput += "<input type='text' id='inputan" + i + "' name='inputan" + i + "'><br>";
			}
			document.getElementById("text-input").innerHTML = textInput;
		}
	</script>
	
</body>
</html>