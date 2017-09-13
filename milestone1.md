<!doctype html>
<html>
<head>
	<meta charset="utf-8">
	<title>Milestone 1 - Part 1</title>
	<link rel="stylesheet" type="text/css" href="normalize.css">
	<link rel="stylesheet" type="text/css" href="style.css">
	<script src="https://code.jquery.com/jquery-2.1.4.min.js"></script>
	<style type="text/css">
		#header {
			background: #184a4a;
			color: #fff;
			padding: 1px 5%;
			box-shadow: 0 1px 3px #555;
			margin: auto;
			text-align: center;
}
		#book{
			width: 80%;
			padding: 1em;
			margin-bottom: 3em;
			margin: 0 auto;
			height: 100%;
			border-bottom-style: solid;
			border-bottom-width: 1px;
		}
		#info{
			float: right;
			width: 60%;
			padding: 1em;

		}
		#pic{
			float: left;
			width: 20%;
			clear: both;
			padding: 1em;
		}
	</style>
</head>
<body>
	<div id="header"><h3>Milestone 1 - Part 1</h3></div>
	<div id="wrapper"></div>
<script>

        $.getJSON("http://it-ebooks-api.info/v1/search/modern%20web", function(json){

            	$.each(json.Books, function(){

            		$('<div class="clearfix" id="book"></div>').append('<img src="' + this.Image + '" id="pic">' 
            			+ '<div id="info">' 
            			+ '<p>' + "<b>Title: </b>" + this.Title + '</p>' 
            			+ '<p>' + "<b>Subtitle: </b>"  + this.SubTitle + '</p>' 
            			+ '<p>' + "<b>Description: </b>"  + this.Description + '</p>' 
            			+ '<p>' + "<b>ID: </b>"  + this.ID + '</p>' 
            			+ '<p>' + "<b>ISBN: </b>"  + this.isbn + '</p>' 
            			+ '</div>').appendTo("#wrapper");

            	});

        }); 
        
</script>
</body>
</html>
