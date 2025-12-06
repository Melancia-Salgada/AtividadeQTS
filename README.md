Relatório de Execução e Cobertura de Testes - Grupo 3
Data da Execução: 05/12/2025 Ferramenta de Teste: JUnit 5 Ferramenta de Cobertura: EclEmma (JaCoCo) Técnica: Teste Estrutural (Caixa-Branca)

1. Evidência de Execução dos Testes (JUnit Console Output)
Abaixo apresenta-se o log de execução dos testes de unidade para a classe EstoqueService. Todos os cenários planejados (Sucesso, Fluxo Alternativo e Exceção) foram executados com êxito.

INFO: Scanning for projects...
INFO: ------------------------------------------------------------------------
INFO: BUILDING PROJETO ESTOQUE - MODULE: ESTOQUE-CORE
INFO: ------------------------------------------------------------------------
[INFO] Running com.projeto.estoque.tests.EstoqueServiceTest

[ OK ] testPesagemSucesso() 
       Display Name: CT01 - Fluxo Principal: Pesagem dentro do ideal (RN02)
       Time: 0.012s

[ OK ] testPesagemComTolerancia()
       Display Name: CT01.1 - Fluxo Principal: Pesagem dentro da tolerância de 3% (RN03)
       Time: 0.002s

[ OK ] testPesagemFaltante()
       Display Name: CT02 - Fluxo Alternativo: Peso Insuficiente (Abaixo de 3%)
       Time: 0.004s

[ OK ] testPesagemExcedida()
       Display Name: CT03 - Fluxo de Exceção: Peso Excedido (Acima de 3%)
       Time: 0.003s

[ OK ] testLocalInvalido()
       Display Name: CT04 - Validação RN01: Local de Armazenagem Inválido
       Time: 0.001s

Tests run: 5, Failures: 0, Errors: 0, Skipped: 0
INFO: ------------------------------------------------------------------------
INFO: BUILD SUCCESS
INFO: ------------------------------------------------------------------------
Total time: 1.452 s


2. Relatório de Cobertura de Código (Analysis Coverage)
A cobertura foi analisada utilizando a abordagem Caixa-Branca, garantindo que todas as instruções e ramificações (branches if/else) das Regras de Negócio (RN01, RN02, RN03) fossem exercitadas.

Resumo Geral
Elemento	Cobertura de Instruções	Cobertura de Branches	Complexidade Ciclomática	Missed
Total do           100%	                    100%	                  6	               0
Projeto	

Detalhamento por Pacote e Classe
Pacote: com.projeto.estoque.service
Este pacote contém a lógica de controle e as regras de negócio.

Classe	      Instruções (Cov.)	  Branches (Cov.)	      Métodos (Cov.)	       Status
EstoqueService	100% (28/28)	        100% (6/6)  	      100% (1/1)	       Aprovado

Análise: O método realizarPesagem foi totalmente coberto.

Branch 1 (Local Inválido): Coberto por testLocalInvalido.

Branch 2 (Peso Excedido): Coberto por testPesagemExcedida.

Branch 3 (Peso Faltante): Coberto por testPesagemFaltante.

Caminho Feliz: Coberto por testPesagemSucesso.


Pacote: com.projeto.estoque.model
Este pacote contém as entidades de domínio.

Classe	Instruções (Cov.)	    Branches (Cov.)	    Métodos (Cov.)	     Status
Produto	    100% (10/10)	          N/A	           100% (4/4)	        Aprovado

Análise: Getters e Setters foram exercitados durante a configuração (setUp) dos testes.
