<%_* 
	template_meta = {
		type:"fleet/car", 
		version:"v1", 
		parts:[
			'template.header',
			'car.data',
			'template.separator',
			'template.footer'
		]
	}
_%>
<% tp.file.include("[[template]]") %>