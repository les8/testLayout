How to start gulp?
1) Create new folder/project
2) Copy and paste there "#src" folder, "gulpfile.js" and "package.json"
3) Open directory with terminal
4) Write the following commands:

   npm i
   npm install webp-converter@2.2.3 --save-dev

5) You should add mixin in (#src/scss/style.scss):

	@mixin font($font_name, $file_name, $weight, $style) {
		@font-face {
			font-family: $font_name;
			font-display: swap;
			src: url("../fonts/#{$file_name}.woff") format("woff"),
				url("../fonts/#{$file_name}.woff2") format("woff2");
			font-weight: #{$weight};
			font-style: #{$style};
		}
	}

	now you must include fonts in this style:
	@include font("Lato", "Lato-Regular", "700", "normal");
   

6) You must write background styles inline to avoid problems:

	background: url("../img/01.png") no-repeat 50% 50%;

7)start gulp! Write the following command in your terminal:

	gulp