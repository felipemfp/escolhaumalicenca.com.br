# Site Escolha Uma Licença

Como o site "Choose Your Own Adventure", mas muito menos interessante.

# Intro

Um grande número de repositórios de GitHub.com não têm uma licença. O GitHub 
fornece um seletor de licença, mas se você não sabe nada sobre licenças, como 
seria possível você tomar uma decisão?

escolhaumalicenca.com.br serve para ajudar pessoas a tomar uma decisão 
consciente sobre licenças.

# Objetivos imediatos

* "Politics Free" - Simplesmente não vamos chegar nisso.
* Bem projeto, mas isso vai ser dizer.
* A página inicial deve ter apenas o suficiente para ajudar 99% das pessoas a 
tomar uma decisão.
* Para o 1% restante, o site irá conter uma lista de licenças comuns para 
comunidades e situações específicas.
* Não compreensiva. Soa como um objetivo estranho, mas há um zilhão (nós contamos) de licenças por aí. Foi preciso filtrar até chegar numa pequena lista com aquelas que realmente importam.

# Rodando na sua máquina

1. `git clone https://github.com/webfatorial/escolhaumalicenca.com.br`
2. `cd escolhaumalicenca.com.br`
3. `script/bootstrap`
4. `script/server`
5. Abra [localhost:4000](http://localhost:4000) no seu browser favorito

# Adicionando uma licença

As licenças estão no diretório `/licenses` em arquivos markdown (`.md`). Cada 
licença tem uma parte inicial em YAML descrevendo as propriedades da licença. 
O corpo do arquivo markdown deve ser o texto da licença. Os campos de metadados 
disponíveis são:

* `title` - O nome da licença
* `layout` - Deve ser `license`
* `permalink` - URL absoluto da licença, começando com `/licenses/`
* `source` - URL para o texto-fonte da licença
* `note` - O campo de nota na barra lateral (opcional)
* `how` - Como usar a licença, também na barra lateral
* `required`, `permitted`, `forbidden` - lista de regras que se aplicam à 
licença (veja abaixo)
* `filename` - O nome do arquivo a ser criado no GitHub.com quando um 
repositório é iniciado com essa licença.

As licenças no escolhaumalicenca.com.br são regularmente importadas no GitHub.com 
para serem usadas como a lista de licenças disponíveis quando um repo é criado. 
Quando criamos um repositório, trocamos certos textos na licença com variáveis 
do repositório. Estas podem ser usadas para criar avisos precisos de direitos 
autorais. As variáveis são:

* `[fullname]` - Nome completo ou username do proprietário do repositório
* `[login]` - Username do proprietário do repositório
* `[email]` - Email principal do proprietário do repositório
* `[project]` - Nome do repositório
* `[description]` - Descrição do repositório
* `[year]` - Ano atual

# Regras 

* Regras (as propriedades da licença) são armazenadas como uma lista dentro do 
trecho YAML das licenças. Uma lista completas de regras pode ser encontrada no 
arquivo `_config.yml` do repositório. Cada regra tem um nome, e.g., 
`include-copyright`, um rótulo legível, e.g., `Copyright inclusion`, e uma 
descrição `Include the original copyright with the code`. Para adicionar uma 
nova regra, simplesmente a adicione em `config.yml` e a referencie na licença 
apropriada.

# Licença

O conteúdo desse projeto, em si, é licenciado sob 
[Creative Commons Attribution 3.0 license](http://creativecommons.org/licenses/by/3.0/us/deed.en_US), 
e o código fonte subjacente usado para formatar e exibir esse conteúdo sob a 
[licença MIT](http://opensource.org/licenses/mit-license.php). 

