# pesquisa-sobre-teoria-dos-conjuntos
- Pesquisa sobre Teoria dos Conjuntos.

## Sobre o website de apresentação
- Comando usado para gerar website:
	- npx create-docusaurus@latest [name] [template] [rootDir]
	- npx create-docusaurus@latest pesquisa-sobre-teoria-dos-conjuntos classic website --typescript
- Versões Utilizadas:
	- nodejs: 22.12.0
	- npm: 10.9.0
	- npx: 10.9.0
	- create-docusaurus: 3.6.3
- Alteração da template:
	- Encontre textos e os substitua:
		- My Site
			- Teoria dos Conjuntos
		- Dinosaurs are cool
			- Tutoriais de Teoria dos Conjuntos
		- Docusaurus Tutorial - 5min
			- Tutoriais - 10 min
		- https://your-docusaurus-site.example.com
			- https://tcarvi.com.br
		- https://github.com/facebook/docusaurus/tree/main/packages/create-docusaurus/templates/shared/
			- https://github.com/tcarvi-engenheiro-eduardo-leal/pesquisa-sobre-teoria-dos-conjuntos/tree/main/
		- Copyright © ${new Date().getFullYear()} My Project, Inc. Built with Docusaurus.
			- atualizado em  ${new Date().toLocaleDateString("pt-BR")} ©TCARVI
		- https://x.com/docusaurus
			- https://x.com/tcarvi_eduardo
		- https://stackoverflow.com/questions/tagged/docusaurus		
			- https://stackoverflow.com/users/26135239/tcarvi-engenheiro-eduardo-leal?tab=questions
		- https://discordapp.com/invite/docusaurus
			- https://www.youtube.com/channel/UCWA39JV7f68QQ6lZEpMOqIA
		- Discord
			- YouTube
		- Hello from $
			- $
		- organizationName: 'facebook'
			- organizationName: 'TCARVI'
		- https://github.com/facebook/docusaurus
			- https://github.com/tcarvi-engenheiro-eduardo-leal/pesquisa-sobre-teoria-dos-conjuntos
	- Se você não usar uma rede social pessoal, exclua textos e links do Facebook.
	- Apague pastas e markdowns do diretório website/docs/, 
		- inclua:
			- /docs/conceitos-gerais/_category_.json
			```json			        {
				"label": "Conceitos Gerais",
				"link": {
  					"type": "generated-index",
  					"description": "5 minutos para ler cada tópico do tutorial."
				}				 	   }  
			```
		- e inclua:
			- /docs/conceitos-gerais/00-conceitos.md
	- Encontre textos e os substitua:
		- /docs/intro
			- /docs/category/conceitos-gerais
- Execução do site, em browser http://localhost:3000
	- ```bash
		cd website
		```    
	- ```bash
		yarn install
		```  
	- ```bash
		yarn start
		```  
