# hello-world
Hello World Repository

This is a note I am leaving in the Read Me file

<!DOCTYPE html>
<html>
	<head>
		  <title>Tabs and Pills</title>
		  <meta charset="utf-8">
		  <meta name="viewport" content="width=device-width, initial-scale=1">
		  <link rel="stylesheet" href="http://maxcdn.bootstrapcdn.com/bootstrap/3.3.6/css/bootstrap.min.css">
		  <script src="https://ajax.googleapis.com/ajax/libs/jquery/1.12.0/jquery.min.js"></script>
		  <script src="http://maxcdn.bootstrapcdn.com/bootstrap/3.3.6/js/bootstrap.min.js"></script>
		  <style>
			div.jumbotron{
				background: linear-gradient(to right, black , cyan);
				color: white;
				padding-left:2%
			}
			canvas{
				background-color: gray;
				border-style: solid;
				margin-left: 10%;
				box-shadow: 0 4px 8px 0 rgba(0, 0, 0, 0.2), 0 6px 20px 0 rgba(0, 0, 0, 0.19);
			}
			canvas:active{
				transition: 6s;
				-ms-transform: rotate(3600deg); /* IE 9 */
				-webkit-transform: rotate(360deg); /* Safari */
				transform: rotate(360deg); /* Standard syntax */
			}
			.form-group{
				margin-left:20%;
				margin-right:20%;
			}
			.all{
			    -webkit-column-count: 2; /* Chrome, Safari, Opera */
				-moz-column-count: 2; /* Firefox */
				column-count: 2;
			}
		  </style>
	</head>
	
	<body>
		<div class="jumbotron">
			<h1>Rainbow</h1>
			<p>Using JavaScript to make a rainbow</p>
		</div>
		<div class="all">
			<div class="form-group">
			  <label for="usr">Height:</label>
			  <input type="number" class="form-control" onchange="can(this.value, usr2.value)" value="300" id="usr1">
			</div>
			<div class="form-group">
			  <label for="usr">Width</label>
			  <input type="number" onchange="can(usr1.value, this.value)" value="300" class="form-control" id="usr2">
			  <br><br><br><br><br><br><br><br><br>
			</div>
			<canvas id="rainbow" height="300px" width="300px">Your browser does not support the Canvas tag</canvas>
		</div>
		<script>
			var c=document.getElementById("rainbow");
			
			function can(x,y){
				document.getElementById("rainbow").style.height= x +"px";
				document.getElementById("rainbow").style.width= y+"px";
				draw();
			}
			
			function draw(){
				//Declaring Canvas and Rectangle as variables
				  //Saving the Canvas to the variable C
				
				var rectangleRed=c.getContext("2d");   //creating a 2D object inside the Canvas
				rectangleRed.fillStyle="red";
				rectangleRed.fillRect(0,0,c.width/7,c.height);    //x1, y1, length of x, length of y
				
				var rectangleOrange=c.getContext("2d");   //creating a 2D object inside the Canvas
				rectangleOrange.fillStyle="orange";
				rectangleOrange.fillRect(c.width/7,0,c.width/7,c.height);    //x1, y1, length of x, length of y
				
				var rectangleYellow=c.getContext("2d");   //creating a 2D object inside the Canvas
				rectangleYellow.fillStyle="yellow";
				rectangleYellow.fillRect((2*c.width)/7,0,c.width/7,c.height);    //x1, y1, length of x, length of y
				
				var rectangleGreen=c.getContext("2d");   //creating a 2D object inside the Canvas
				rectangleGreen.fillStyle="green";
				rectangleGreen.fillRect((3*c.width)/7,0,c.width/7,c.height);    //x1, y1, length of x, length of y
				
				var rectangleCyan=c.getContext("2d");   //creating a 2D object inside the Canvas
				rectangleCyan.fillStyle="cyan";
				rectangleCyan.fillRect((4*c.width)/7,0,c.width/7,c.height);    //x1, y1, length of x, length of y
				
				var rectangleBlue=c.getContext("2d");   //creating a 2D object inside the Canvas
				rectangleBlue.fillStyle="blue";
				rectangleBlue.fillRect((5*c.width)/7,0,c.width/7,c.height);
				
				var rectanglePurple=c.getContext("2d");   //creating a 2D object inside the Canvas
				rectanglePurple.fillStyle="purple";
				rectanglePurple.fillRect((6*c.width)/7,0,c.width/7,c.height);
			}		
		</script>
		
	</body>
</html>
