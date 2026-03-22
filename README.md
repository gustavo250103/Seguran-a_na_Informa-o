# Verificação de Hashes (SHA256 e MD5)

Utilitário em Python que demonstra, de forma simples, como calcular e comparar hashes SHA256 e MD5 de textos. Serve como exemplo acadêmico e portfólio: mostra boas práticas de organização de código, geração de relatórios automatizados e versionamento de evidências em histórico.

## Como funciona
- Lista fixa de textos com os respectivos hashes esperados (SHA256 e MD5) está definida em `src/verifica_hashes.py`.
- O script calcula os hashes em UTF-8, compara com os valores esperados e marca cada item como **Verdadeiro** (ambos corretos) ou **Falso** (pelo menos um diverge).
- Gera `verificacao_hashes.txt` (sempre sobrescrito) e uma cópia datada em `historico/verificacao_hashes_YYYYMMDD_HHMMSS.txt` para manter o histórico de execuções.
- O README é estático — rodar o script não altera este arquivo.

## Como executar
- Requisito: Python 3.8 ou superior.
- Comando: `python src/verifica_hashes.py`
- Saída esperada: mensagens no terminal indicando sucesso e os arquivos de relatório atualizados.

## Estrutura gerada
- `verificacao_hashes.txt` — relatório mais recente com hashes calculados, esperados, status e erros detalhados.
- `historico/` — arquivos de relatórios anteriores com carimbo de data e hora.
- `src/verifica_hashes.py` — código-fonte principal.

## Tabela de referência (dataset atual)
Verdadeiro = SHA256 e MD5 correspondem; Falso = alguma divergência.

| Texto | Verdadeiro/Falso |
| --- | --- |
| A primeira das instituições criadas pelo Pe. Roberto Sabóia de Medeiros foi a antiga Escola Superior de Administração de Negócios de São Paulo - ESAN/SP. | Verdadeiro |
| A FEI é uma instituição vinculada estatutariamente à Companhia de Jesus | Falso |
| Em 20 de janeiro de 1951 foi realizada a sessão solene da congregação para a Colação de Grau da primeira turma da Faculdade de Engenharia Industrial. | Verdadeiro |
| A Capela Santo Inácio de Loyola foi construída no ano de 1978, em concreto aparente. | Falso |
| Tendo como função principal a promoção do aprimoramento profissional no campo administrativo e tecnológico, o IECAT (Instituto de Especialização em Ciências Administrativas e Tecnológicas) foi criado em 1982 | Verdadeiro |
| Dentro de uma proposta de integração e de agregação de competências, visando a excelência de seus cursos, as instituições FEI, FCI e ESAN foram transformadas no Centro Universitário da FEI no ano de 2002. | Falso |
| O Centro Universitário da FEI passou a fazer parte do seleto grupo que produz ciência no Brasil, quando a CAPES aprovou o primeiro curso de Mestrado em Engenharia Elétrica em 2005. | Verdadeiro |
| Em 2016 foi realizada a primeira edição do congresso de inovação - Megatendências 2050. | Verdadeiro |
| Em 2012 o Centro Universitário FEI celebrou 70 anos de história e de excelência na inovação e na formação de mais de 50 mil profissionais altamente qualificados para o setor empresarial, entre Administradores, Engenheiros e Cientistas da Computação. | Verdadeiro |
| Em 1999 iniciam-se as atividades da FCI (Faculdade de Informática), como o curso de Ciência da Computação. | Falso |
| SHA256 e MD5 corretos | Verdadeiro |
| Somente SHA256 correto | Falso |
| Somente MD5 correto | Falso |
| Nenhum dos dois corretos | Falso |

## Por que usar este projeto
- Demonstração clara de hashing e verificação de integridade.
- Geração automática de evidências com versionamento em histórico.
- Código curto, legível e fácil de apresentar em sala de aula ou em um repositório público.
