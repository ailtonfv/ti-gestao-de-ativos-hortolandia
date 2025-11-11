# Dicionário de Campos — Inventário de Ativos de TI

Este documento descreve, de forma objetiva, cada campo da **planilha_mestra.csv** utilizada no inventário.

| Campo | Tipo | Descrição | Obrigatoriedade | Observações |
|---|---|---|---|---|
| unidade_sigla | texto | Sigla oficial da Unidade/Secretaria | obrigatório | Ex: SMED, SMS, SEAS |
| localizacao | texto | Sala / setor / andar | obrigatório | Descrição livre |
| tipo_equipamento | enum | desktop / notebook / impressora / servidor / outros | obrigatório | Se “outros”, especificar em observações |
| marca | texto | Fabricante do equipamento | obrigatório | Ex: Dell, Lenovo, HP |
| modelo | texto | Modelo comercial | obrigatório | Ex: Optiplex 3080 |
| numero_serie | texto | Número de série do hardware | obrigatório | Se ausente, justificar |
| responsavel_nome | texto | Nome do usuário responsável | obrigatório | Conforme cadastro interno |
| responsavel_matricula | texto | Matrícula funcional | obrigatório | Conforme RH |
| situacao_conectividade | enum | online / offline | obrigatório | Se offline → campos de rede podem ficar vazios |
| id_rede | texto | Hostname na rede | condicional | Exigido se conectividade = online |
| mac_address | texto | Endereço MAC | condicional | Formato: AA:BB:CC:DD:EE:FF |
| ipv4 | texto | Endereço IPv4 | condicional | Ex: 10.0.5.12 |
| sistema_operacional | texto | Nome + versão | obrigatório | Ex: Windows 10 22H2 / Ubuntu 22.04 |
| antivirus | texto | Nome do antivírus ou “não possui” | obrigatório | Ex: Windows Defender |
| softwares_corporativos | texto | Lista separada por “;” | opcional | Ex: SEI; SIGAS; e-SUS |
| ano_aquisicao | número (AAAA) | Ano de aquisição | obrigatório | Validado entre 2013 e ano vigente |
| estado_geral | enum | operacional / precisa_manutencao / sucata | obrigatório | Usado em decisão de renovação |
| observacoes | texto | Comentários livres | opcional | Justificativas e observações adicionais |

---

## Observação sobre ferramentas
A Prefeitura utiliza **software livre LibreOffice** para edição e envio das planilhas.  
Formato recomendado de trabalho: **CSV (UTF-8, separador vírgula)**.

---

## Referências
- COBIT 2019 — BAI09 (Manage Assets)
- ITIL 4 — Service Configuration Management
- ISO/IEC 20000-1:2018 — Gestão de Serviços de TI
