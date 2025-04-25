
# Documentation of Basic Concepts about CSS use / Documentação de tudo que utilizei de conceitos basicos do CSS (Portuguese/English)

## Descrição geral
    Este Arquivo apresenta a descrição de um resumo pessoal, dos meus estudos que utilizaei para consultar e desenvolver os sites e os elementos que constam nesse repositório. É mais um resumo de fácil Acesso. Espero que você também possa tirar proveito disso, sinta-se livre pra consultar esse Readme sempre que precisar entender alguma função usada. 
    Geralmente costumo documentar as funções dentro do código também.

## General Description
This document provides a summary of my studies used to reference and develop websites and the elements in this repository. It is designed for quick and easy access. Feel free to consult this README whenever you need help understanding a feature. I usually document functions directly within the code as well.

## **Tipos de Formatação:**

### **1. Formatação Inline Style**
- Esta formatação é utilizada dentro do operador de cada parágrafo
#### **1.1 Clacificação de COR**
```html
    -<p style="color: green"> Parágrafo </p> 
```
A caracterização CSS nesse formato é dado pelo categorizador "style, dentro do operador do parágrafo.
O aprâmetro **color: cor_em_inges**, dentro do parâmetro **style=""** define a cor do parágrafo
Perceba qu epodemos mudar a cor a vontade desntro deste parâmetro, mas dentro da tag de cada parágrafo.

#### **1.2 Formatação CSS INTERNO com seletores**
- Esta formatação, é inserida dentro da tag de Head e é utilziada para manipular seletores para formatar varias tags HTML de uma vez
```html
    <head>
        <style>
            p {color: red} 
            h1 {color: red} 
        </style>
    </head>
```

## **3. Classes e IDs**
- **O que são os ID's?** Os ID identificam elementos unicos, ou seja é a identidade única de cada elemento. Funciona como o nosso documento de identificação nacional, ele é único por pessoa.
- **O que são as Classes?** As Classes são vários itens em conjunto. Ou seja, a classe é uma classificação de um grupo de individuos ou de apenas um indivíduos, mas é um grupode pertencimento.
```html 
    <head>
        <style>
            p {color: red;} 
            .azul {blue}
            #principal {background:gray;}
            .produto {background: lightyellow; margin: 10px}
        </style>
    </head>
```
- Desta fora, definimos a cor dos paragráfos padrão como RED, vaemelha, e criamos a classe **.azul** e podemos utilizalas dentro da tag do paragrafo. 
- Também definimos um ID **#principal** e podemos utiliza-lo dentro da tag também. Para destacar um elemento único.
- Recomenda-se o ID para configurações Únicas e recomensa-se a classe para recomendações plurais, mas que são a minoria.
- Perceba que utilizamos um novo **CATEGORIZADOR**: O Background que define o fundo de um elemento.
```html
    <p class="azul"> Parágrafo </p>
    <p id="principal"> Parágrafo </p>
```
## **4. Tags Div e Span**
- As **div** são tags utilizadas para enquandrutar, separar e agrupar elementos facultamente dentro do seu site. Ou seja, separar o projeto por sessões, categorias ou até posicionamento. Elas auxilial na classificação, organização e efluidez do proejto.

```html
<body>
    <div id="conteudo">
	<div class="produto"> Produto 1 </div>
	<div class="produto"> Produto 2 </div>
	<div class="produto"> Produto 3 </div>
</body>
```
- Formatação pra cada Elemento da **div** e para o conjunto todo.

- Já o Span é feito para eliminar os espaços entre os elementos, ficando cada um na junção de seus elementos por exemplo: Produto 1 Produto 2 Produto 3. Seria como se voe só escrevesse.
```html
<body>
    <div id="conteudo">
	<span class="produto"> Produto 1 </span>
	<span class="produto"> Produto 2 </span>
	<span class="produto"> Produto 3 </span>
</body>
```

## **5. Bordas**
- Bordas de qualquer Elemento CSS
```html
<head>
	<style type="text/css">
		#conteudo {border: 3px solid red;}
	</style>
</head>
```
Dessa forma, temos 3 parametros variáveis qu epodemos definir. Os pixels **px**; o comportamento do traço **solid** e a cord do traço ou apresentação **red**.
- Também é possível fazer elemento por elemento. Ex:
```html
<head>
	<style type="text/css">
		#cabeca {border-color: red green yellow purple; border-width: 15px 10px 20px 10px; border-style:solid dotted dashed double;	}
	</style>
</head>
```

## **6. Fontes e Cores**
### **6.1 Cores**
- As fomratações podem ser inseridas como <style> na <head>, assim como visto acima.
- As cores podem utilizar as padrões como "red", "blue" etc, ou podemos disponibilizar o código # da cor. Peado numa tabela qualquer na internet. 
- Recomendação de site: https://htmlcolorcodes.com/
- Inserir Cor: <tag color: cor;> </tag>
```html 
    <head>
       <style type="text/css"> 
		.formato { color: #DA70D6;font-size: 30px; }
	</style>
    </head>
```
#### **6.2 Fontes**
- Inseridas dentro ed uma formatação ou dentro de uma <tag>. Geralmente acompanhado em uma Classe ou ID. Assim como as cores.
```html
<head>
    <style type="text/css"> 
		.formato { color: #DA70D6; font-family: "Palatino Linotype", Palatino, "Times New Roman", Times, serif; font-size: 35px;}
	</style>
</head>
```

### **6.3 Textos e Tamanhos**

- Medidas de tamanho mais comuns:
    - px (fixo)
    - % (relativo à tela)
    - em (Rrelativa de acordo com o container pai. Deixa tudo de acordo com uma proporção correta.)

```html
    <style type="text/css">
			div {font-size: 30px;}
			.texto {font-size: 2em;}
	</style>
```
Assim, tudo que ficar dentro dos containers **div**, da classe .texto, ficara com o dobro de tamanho, por exemplo.

### **6.4 Textos e ESTILOS**
- Interessante inserir os estilos dentro de um style
- Posso acumular todas dentro do comando ***font***
- Podemos fazer separadamente

```html
<head>
	<style type="text/css">
		body {font-size: 40px; font-family: "Times New Roman", Times, serif;}
		.negrito {font-weight: 900;}
		.italico {font-style: italic;}
		.formatacao {text-decoration: line-through;}
		.tudo {font: 50px; color: green; text-decoration: line-through; font-family: "Times New Roman",sans-serif; font-weight: bolder;}
	</style>
</head>
<body>
	<p class="negrito"> Um texto de teste AQUI.</p>
	<p class="italico"> Um texto de teste AQUI.</p>
	<p class="formatacao"> Um texto de teste AQUI.</p>
	<p class="tudo"> Um texto de teste AQUI.</p>
	<p> Um texto de teste AQUI.</p>
</body>
```
### **7. Imagem e Cor de Fundo**
- Função geral de cor de fundo: ***bacground-color: codigo da cor***
- Funções de ***background*** manipulam o fundo
- ***background-image: url('texto')*** imput uma imagem de fundo.
- ***background-atachment***:  define o comportamento da imagem (scroll; fixed)
```html
<head>
	<style type="text/css">
		.fundo {background: yellow scroll center no-repeat url('imagens/yoshi.png');}
		.yoshi {background-image: url('imagens/yoshi.png'); background-repeat: repeat-x; background-attachment: fixed; background-position: center; background-color: lightyellow;}
	</style>
</head>
<body class="fundo"></body>
```

## **7. Formatação CSS Exterson**
- Basicamente, para padroinizar e centralziar as configurações de estilo de seu projeto, voce pode salvar uma aba externa, ou seja, um arquivo estilizado .css por fora e referencialo em suas páginas sempre que quiser usar os estilos dele. Assim, voce pode alterar as configurações dele somente, pr amudar tudo de uma vez.
- **Passo 1: Faça o arquivo estilziado e salve com a extenção ***.css***
- **Passo 2: Referêncie a página do arquivo na sua página de trabalho**
*Como possso referencialo?*
```html
<head>
	<link rel="stylesheet" type="text/css" href="estilo.css">
</head>
```
O link no href deve conter as subpastas, se houver.


# ENGLISH
## **Formatting Types:**

### **1. Inline Style Formatting**
- This formatting is applied directly inside the tag of each paragraph.
#### **1.1 Color Classification**
```html
<p style="color: green"> Paragraph </p>
```
CSS styling in this format is defined by the "style" attribute inside the paragraph tag. The parameter **color: color_in_English**, inside the **style=""** attribute, sets the color of the paragraph. You can change the color freely within this parameter, but it applies only to that specific paragraph tag.

### **1.2 Internal CSS with Selectors**
- This formatting is inserted into the `<head>` tag and is used to manipulate selectors for formatting multiple HTML tags at once.
```html
<head>
    <style>
        p {color: red;} 
        h1 {color: blue;} 
    </style>
</head>
```

## **2. Classes and IDs**
- **What are IDs?** IDs identify unique elements, much like a unique identification number.
- **What are Classes?** Classes group elements together for collective styling.
```html
<head>
    <style>
        p {color: red;} 
        .blue {color: blue;}
        #main {background: gray;}
        .product {background: lightyellow; margin: 10px;}
    </style>
</head>
```
IDs are used for unique styling, while Classes are used for grouping similar elements. Use `#` for IDs and `.` for Classes.

## **3. Div and Span Tags**
- **Div** tags are used for grouping and separating sections of content.
```html
<body>
    <div id="content">
        <div class="product"> Product 1 </div>
        <div class="product"> Product 2 </div>
        <div class="product"> Product 3 </div>
    </div>
</body>
```
- **Span** tags are used for inline grouping.
```html
<body>
    <span class="product"> Product 1 </span>
    <span class="product"> Product 2 </span>
    <span class="product"> Product 3 </span>
</body>
```

## **4. Borders**
- Borders can be applied to any CSS element.
```html
<head>
    <style>
        #content {border: 3px solid red;}
    </style>
</head>
```
You can customize border width, style, and color using properties like `border-width`, `border-style`, and `border-color`.

## **5. Fonts and Colors**
### **5.1 Colors**
- Colors can be specified as names (e.g., "red", "blue") or as hexadecimal codes.
- Example:
```html
<head>
    <style>
        .styled {color: #DA70D6; font-size: 30px;}
    </style>
</head>
```

### **5.2 Fonts**
- Fonts are defined using the `font-family` property.
```html
<head>
    <style>
        .styled {font-family: "Palatino Linotype", Palatino, "Times New Roman", serif; font-size: 35px;}
    </style>
</head>
```

## **6. Backgrounds**
- Backgrounds can be styled using `background-color` or `background-image`.
```html
<head>
    <style>
        .background {
            background: yellow scroll center no-repeat url('images/example.png');
        }
    </style>
</head>
<body class="background"></body>
```

## **7. External CSS**
- Save styles in a `.css` file and link it to your HTML document:
```html
<head>
    <link rel="stylesheet" type="text/css" href="styles.css">
</head>
```
This allows centralized style management for your project.

Thanks For reading :D
