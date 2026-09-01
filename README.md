# Generic Photovoltaic Simulated Interconnection Application PT_BR
Simulated Interconnection Application on a photovoltaic residential project.

## Included documents

- **Excel PV dimensioning spreadsheet** — sizing, string configuration and payback (Law 14.300/2022)
- **PVsyst simulation report** — annual yield and performance ratio
- **Technical design report** — full technical specification for utility interconnection
- **Single-line diagram** — protection and equipment layout

*Known error: my single-line diagram has a risked text. It is because my program bugged and i didn't want to restart the project. Frequent saves and eventually getting to know how it ocurred will make other diagrams made by me not come with a risked text.

## Checklist - CPFL Energia São Carlos:

**Checklist de Homologação**

Sistema fotovoltaico conectado à rede

**Escopo: **micro e minigeração distribuída (MMGD), Grupo B.

**Base normativa: **Lei 14.300/2022 · REN ANEEL 1.000/2021 · REN ANEEL 1.059/2023 · PRODIST Módulo 3 Seção 3.7 · PRODIST Módulo 8 · Portarias INMETRO 140/2022 e 515/2023 · NBR 16149 / 16150 / 16274 / 16690 / 5410 / 14039 / 5419 · norma técnica da distribuidora (CPFL: GED-15303).

**Regra de ouro: **um item faltando devolve o processo inteiro e reinicia parte da contagem de prazo. Marcar item por item antes de protocolar sai mais barato que corrigir depois.

# **Fase 0 — Enquadramento**

*Antes de desenhar qualquer coisa.*

- Potência instalada em CA definida (é o inversor, não o arranjo — ex.: 5,0 kVA para um arranjo de 5,5 kWp)

- Enquadramento: microgeração ≤ 75 kW · minigeração > 75 kW

- Confirmado que não há fracionamento da central em unidades menores (expressamente vedado)

- Modalidade da Lei 14.300 definida: autoconsumo local / autoconsumo remoto / geração compartilhada / EMUC

- Titular da UC confere com o CPF/CNPJ da conta de energia

- Tipo de ligação e tensão anotados (mono / bi / trifásico, 220/127 V)

- Potência disponibilizada da UC calculada e ≥ potência do inversor (ex.: 32 A × 220 V = 7,04 kVA)

- Versão vigente da norma da distribuidora baixada e conferida (elas mudam sem aviso)

# **Fase 1 — Equipamentos**

- Inversor com registro INMETRO válido — número e data anotados

- Módulos com registro INMETRO — número, importador e data anotados

- Inversor consta na lista de equipamentos aceitos pela distribuidora, quando ela mantém uma

- Datasheets em versão brasileira arquivados (se o modelo for rebadge, guardar também o datasheet do fabricante original — costuma ter os campos que faltam)

- Do módulo: Voc, Vmp, Isc, Imp, coeficientes de temperatura

- Do inversor: faixas de tensão e frequência de operação, corrente máxima de saída, nº de MPPTs

- Ajustes de proteção e anti-ilhamento conforme NBR 16149

- Compatibilidade string × MPPT verificada: Voc na temperatura mínima do local abaixo da tensão máxima do inversor; corrente por MPPT respeitada

# **Fase 2 — Projeto elétrico**

- Diagrama unifilar assinado, cobrindo lado CC e CA, proteções, seccionamento, aterramento e medição

- Diagrama de blocos

- Seções de condutores dimensionadas (CC e CA) — e iguais às citadas no memorial

- Proteção CA: disjuntor com curva e polaridade corretas + DPS CA

- Proteção CC: chave seccionadora, fusíveis de string, DPS CC com tensão compatível com a string

- Aterramento e SPDA (NBR 5419)

- Planta de localização com coordenadas e número do poste de conexão

- Layout de disposição dos módulos no telhado

- Memorial descritivo com: consumo médio da UC, irradiação (fonte e valor declarados), rendimento adotado, geração estimada mensal e % de cobertura do consumo

## **Verificação cruzada — onde a maioria dos processos trava**

Os mesmos números precisam aparecer idênticos no memorial, no unifilar, na planilha de dimensionamento e no datasheet:

- Modelo e potência do inversor

- Modelo e potência dos módulos, e quantidade

- Tensão de string (Voc a frio, não a de operação)

- Corrente de saída CA

- Seção dos cabos

- Tensão nominal dos DPS

- Potência instalada declarada no formulário

# **Fase 3 — Pacote documental**

- Formulário de solicitação de acesso (Anexo II, III ou IV da Seção 3.7, conforme a potência)

- ART do responsável técnico, paga e assinada — projeto e execução

- Projeto elétrico + memorial descritivo

- Diagrama unifilar e de blocos

- Certificado / registro de conformidade do inversor

- Documento de identificação do titular + conta de energia recente

- Procuração, se quem protocola não é o titular

- Lista de unidades consumidoras com percentual de rateio (autoconsumo remoto, geração compartilhada, EMUC)

- Instrumento jurídico de solidariedade (geração compartilhada e EMUC)

# **Fase 4 — Protocolo, parecer e vistoria**

- Protocolo feito pelo sistema eletrônico da distribuidora; número guardado

- Parecer de acesso: 15 dias (micro) ou 30 dias (mini) — dobra se houver obra ou reforço de rede

- Parecer lido linha a linha: condicionantes técnicas, ajustes de proteção exigidos, troca de medidor, eventual custo de obra

- Obra executada conforme o projeto aprovado (qualquer alteração exige reapresentação)

- Vistoria solicitada em até 120 dias contados do parecer

- Vistoria realizada em até 7 dias da solicitação; relatório de pendências em até 5 dias úteis

- Pendências sanadas e reapresentadas

- Aprovação do ponto de conexão + medidor bidirecional instalado

- Relacionamento Operacional (micro) ou Acordo Operativo (mini) assinado

# **Fase 5 — Comissionamento e fechamento**

*Conforme NBR 16274.*

- Continuidade do condutor de aterramento

- Resistência de isolamento do lado CC

- Polaridade e Voc / Isc medidos por string, comparados ao projeto

- Teste de desligamento e resposta anti-ilhamento

- Relatório de comissionamento assinado

- Manual de O&M e datasheets entregues ao cliente

- Primeira fatura conferida: energia injetada, créditos e cobrança do fio B conforme o cronograma da Lei 14.300

# **Erros recorrentes que devolvem o processo**

| **Erro** | **Onde aparece** |
| --- | --- |
| Potência instalada declarada como kWp do arranjo em vez de kVA do inversor | Formulário |
| Voc calculado na temperatura ambiente em vez da mínima | Memorial / unifilar |
| Seção de cabo divergente entre memorial e unifilar | Verificação cruzada |
| DPS CC especificado com tensão de outro projeto | Unifilar |
| ART sem a atividade de execução | Pacote documental |
| Inversor sem registro INMETRO vigente | Fase 1 |
| Número do poste em branco | Planta de localização |
| Norma da distribuidora em versão desatualizada | Fase 0 |
