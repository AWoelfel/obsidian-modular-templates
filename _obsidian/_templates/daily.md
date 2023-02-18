<%_* 
	template_meta = {
		type:"daily", 
		version:"v1", 
		parts:[
			'daily.header',
			'template.separator',
			'daily.body',
			'template.separator',
			'template.footer'
		]
	}
_%>
<% tp.file.include("[[template]]") %>