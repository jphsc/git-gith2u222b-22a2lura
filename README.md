# Criando um arquivo direto no site do github

> Status: Iniciando no curso

```
node app.js
```

<h2>Comandos do git</h2>
<h3>git clone urlDoProjeto</h3>
<p>Clona o repositório existente no github para a máquina (local). Quando queremos clonar um repo criando uma nova branch para ele, usamos o comando 'git clone -branch nomeDaBranch urlDoProjeto'</p>

<h3>Criando um repositório local e integrando com um repositório remoto</h3>
<ul>
 <li>Criar o arquivo do git no repositório: git init</li>
 <li>Criar o readme: git add README.md</li>
 <li>Primeiro commit: git commit -m "comentario desejado"</li>
 <li>Selecionar a branch main: git branch -M main</li>
 <li>Interligar o repositório local com o remoto: git remote add origin https://github.com/jphsc/t.git</li>
 <li>Subir as alterações para o remoto: git push -u origin main</li>
</ul>

<h3>Carregando os itens do repositório remoto</h3>
<ul>
 <li>Interligar o repositório local com o remoto: git remote add origin https://github.com/jphsc/t.git</li>
 <li>Selecionar a branch main: git branch -M main</li>
 <li>Subir as alterações para o remoto: git push -u origin main</li>
</ul>

<h3>git log</h3>
<p>Retorna o histórico das últimas alterações.</p>
<p>Para retornar todos os históricos (commits) desde a criação do repositório, deve-se executar<strong>git log --oneline</strong>.</p>

<h3>git pull</h3>
<p>Obtém as atualizações da origem para o local. Também pode ser utilizado 'git pull urlDoProjeto', dependendo das configurações locais.</p>

<h3>git status</h3>
<p>Retorna o status dos arquivos, quais foram modificados, etc</p>

<h3>git commit ?arquivo/.? -m "descrição do commit"</h3>
<p>O git commit pode ser executado como 'git commit arquivo.extensao -m "descrição do commit" ' quando o arquivo editado já existe no repositório original e já foi adicionado, caso ele seja novo, precisa ser adicionado ao repositório local. Caso sejam vários arquivos que já existem no reposiório original, não especificamos o arquivo dessa forma 'git commit . -m "descrição do commit"'</p>

<h3>git push </h3>
<p>O push é utilizado para "finalizar" a edição, ou seja, efetivar o commit para a origem, ele 'empurra' para a origem os commits, podendo haver mais de um commit realizado. O comando do push para adicionar na branch original é 'git push origin main', caso fosse uma outra origem, tipo uma branch de desenvolvimento o comando seria 'git push origin desenvolvimento'</p>

<h3>git add</h3>
<p>É o comando para adicionar novos arquivos ao repositório remoto, caso esteja sendo adicionado um arquivo o comando é 'git add "nome do arquivo" ', para adicionar todos os novos arquivos, também pode ser utilizado 'git add .' ou 'git add -A'</p>

<h3>git restore --source valorDoHash nomeArquivo/.</h3>
<p>É o comando para retornar para alguma versão, sendo necessário informar o hash que pode ser obtido com o comando 'git log --oneline' ou apenas 'git log' quando é sabe-se que a é a o último push. Quando o interesse é em voltar apenas um arquivo é necessário informar o nome.extensao sendo o comando 'git restore --source valorDohASH nomeDoArquivo.extensao' ou caso deseja-se a restauração de todos os arquivos daquele hash o comando é 'git restore --source valorDohASH .'</p>

<h3>git checkout -b nomeDaBranch</h3>
<p>Podemos criar novas branchs e mudar automaticamente para essa branch, muito comum em projetos grandes, evitando quebrar o código principal.
O 'git checkout -b nomeDaBranch' cria uma branck e já troca pra ela. O 'git checkout nomeDaBranch' apenas cria uma branck sem trocar pra ela.</p>

<h3>git switch nomeDaBranch</h3>
<p>Para sair de uma branch e 'entrar noutra', similar ao git checkout.</p>

<h3>git branch</h3>
<p>Mostra todas as branchs que temos.</p>

<h3>git merge nomeDaBranchAJuntar</h3>
<p>O merge é o processo de 'trazer' todos os pushs de outras branchs para a main.
Primeiro devemos estar na branch que queremos trazer as mudanças (git switch nomeDaBranchOrigem),
Segundo devemos fazer o merge da branch que queremos trazer (git merge nomeDaBrachDestino),
Terceiro é fazer o push na branch origem (git push origin nomeDaBranchOrigem)
</p>

<h4>Mais informações sobre como escrever um readme.md mais estiloso, seguir: <a href="https://www.alura.com.br/artigos/escrever-bom-readme">este link</a>.</h4>
