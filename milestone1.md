<html>
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
