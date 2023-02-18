<%_* 
	template_parts = [
		'template.header', 
		template_meta.type + '.data', 
		'template.separator', 
		template_meta.type + '.body',
		'template.separator', 
		'template.footer'
	]

	if (template_meta.parts) {
		template_parts = template_meta.parts
	}

	template_content = ""
	
	for (let i = 0; i < template_parts.length; i++) {
		template_content += await tp.file.include("[[" + template_parts[i] + "]]")
	}
	
	tp.file.move(template_meta.type + "/" + tp.file.title)
_%>
<% template_content %>