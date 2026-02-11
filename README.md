# Modelos de Classificação para Estimativa do Salário Mínimo Necessário (2023)

## Descrição do Projeto

Este Trabalho de Conclusão de Curso (TCC) tem como objetivo desenvolver e avaliar **modelos de classificação supervisionada** capazes de prever se um indivíduo atinge o patamar do **Salário Mínimo Necessário**, considerando um cenário com **dois provedores no domicílio**, com base no valor divulgado para o ano de 2023.

O problema foi estruturado como uma **classificação binária**, utilizando dados socioeconômicos da **PNAD Contínua (IBGE)** e técnicas de aprendizado de máquina aplicadas a dados reais de âmbito nacional.

---

## Base de Dados

Os dados utilizados são provenientes da **Pesquisa Nacional por Amostra de Domicílios Contínua (PNAD Contínua)**, disponibilizada pelo Instituto Brasileiro de Geografia e Estatística (IBGE).

Fonte dos Dados: https://ftp.ibge.gov.br/Trabalho_e_Rendimento/Pesquisa_Nacional_por_Amostra_de_Domicilios_continua/Anual/Microdados/Trimestre/Trimestre_1/Dados/

Fonta da Documentação Técnica: https://ftp.ibge.gov.br/Trabalho_e_Rendimento/Pesquisa_Nacional_por_Amostra_de_Domicilios_continua/Anual/Microdados/Trimestre/Trimestre_1/Documentacao/

### Como conectar a base de dados ao código?

Optou-se por realizar o procedimento abaixo para garantir flexibilidade e agilidade no desenvolvimento da aplicação. Segue o passo a passo:
- Realize o download do arquivo a partir da fonte de dados citada anteriormente e exporta para o Google Drive.
- No Google Colab, vá em arquivos no canto esquerdo e permite conectar ao Google Drive.
- Procure o arquivo, copia o caminho e substitua no link a seguir em seu notebook: /content/drive/MyDrive/Arquivo_IBGE/PNADC_2023_trimestre1.txt
- Esta célula encontra-se em Seleção de features e de rótulo para criação dos DataFrames > 1° Trimestre de 2023

<img width="785" height="614" alt="image" src="https://github.com/user-attachments/assets/8bb765e8-213b-4c5b-940f-5d4fa559a056" />


---

## Construção da Variável Alvo

A variável alvo foi construída com base no **Salário Mínimo Necessário**, divulgado pelo DIEESE para o ano de 2023.

Fonte: https://www.dieese.org.br/analisecestabasica/salarioMinimo.html#2023

### Procedimento Metodológico

1. Identificação do valor do salário mínimo necessário em 2023.
2. Divisão do valor por **2 provedores**, hipótese adotada no estudo.
3. Criação da variável binária
