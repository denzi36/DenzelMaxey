<!DOCTYPE html>
<html>
<head>
<title>Milestone 1 Part 1</title>
<script src="https://code.jquery.com/jquery-2.1.4.min.js"></script>
<style>


#header {
		background-color: #cbc9c9;
		width: 90%;
		margin: 0 auto;
		height: 80%;
		margin-top: -10px;
	}
	
	.previousPage {
		color: #000000;
		font-style: bold;
		float: left;
		margin-top: -30px;
		margin-left: 10px;
	}
	
	a {
		color: #000000;
		font-style: bold;
	}
	
	a:visited {
		color: #ffffff;
	}
	
	a:hover {
		color: red;
	}
	
	.heading-text {
		text-align: center;
		padding-top: 20px;
		color: #000000;
	}
		
	#books {
		background-color: #cbc9c9;
		margin-top: 15px;
		padding-bottom: 30px;
		width: 90%;
		margin: 0 auto;	
		border: 2px solid red;
	}
	
	img {
		float: left;
		margin-left: 30px;
		margin-right: 20px;
		border: 2px solid black;
		width: 204px;
		height: 250px;
		margin-bottom: 30px;
	}
	
	h2 {
		margin-top: -5px;
	}
	
	h4 {
		font-style: italic;
		margin-top: -15px;
	}	
	
	.description {
		margin-right: 80px;
	}
	</style>
			<script>
			$.getJSON('http://it-ebooks-api.info/v1/search/modern%20web', function(data) {
			$.each(data.Books, function(){
				$('<br><div class="results"></div>').append(
				
						'<div id="books">' + '<br><img src="' + this.Image + '">' + '<p><h2>' + this.Title +  ':</h2>' + '<h4>'+ this.SubTitle + '</h4></p>' + 
						'<p><b>ID Number:&nbsp;&nbsp;</b>' + this.ID + '</p>' + '<p ><b>ISBN:&nbsp;&nbsp;</b>' + this.isbn + '</p> ' + 
						'<p class="description"><b>Description:&nbsp;&nbsp;</b><em>' + this.Description + '</em></p>' + '<br></div>'
					
				).appendTo("body");
			
			})
		
		
		});
	</script>
	</head>
	
	<body>
		
<div id = "header">
		<h1 class="heading-text">Milestone 1 Part 1</h1>
		<p class="previousPage"><a href="/index.html">Return to Main Page</a></p>
		</div>				
			
	</body>
</html>
