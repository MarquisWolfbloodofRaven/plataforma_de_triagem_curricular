# plataforma_de_triagem_curricular
# 📋 Triagem de Currículos

Uma aplicação web para facilitar e agilizar o processo de triagem de currículos, permitindo comparar candidatos com os requisitos de uma vaga, identificar qualificações e organizar resultados de forma simples e visual.

O projeto funciona diretamente no navegador, sem necessidade de backend ou envio de arquivos para servidores externos.

## ✨ Funcionalidades

- **Leitura de currículos:** suporte a arquivos PDF, DOCX, TXT e imagens (JPG, JPEG e PNG).
- **Reconhecimento de texto (OCR):** utiliza Tesseract.js para extrair informações de currículos digitalizados ou enviados como imagem.
- **Requisitos obrigatórios:** permite definir competências e qualificações indispensáveis para a vaga.
- **Requisitos desejáveis:** adiciona critérios complementares que aumentam a pontuação dos candidatos.
- **Experiência profissional:** permite estabelecer um tempo mínimo de experiência.
- **Formação acadêmica:** possibilita definir o nível mínimo de escolaridade.
- **Localização:** permite verificar se o currículo menciona uma cidade ou região específica.
- **Pontuação automática:** calcula uma pontuação de compatibilidade com base nos critérios definidos.
- **Classificação de candidatos:** organiza os resultados em três categorias:
  - 🟢 **Forte:** pontuação igual ou superior a 75%, sem requisitos obrigatórios pendentes.
  - ⚪ **Possível:** atende aos requisitos obrigatórios, mas apresenta pontuação inferior a 75%.
  - 🔴 **Não atende:** não possui um ou mais requisitos obrigatórios identificados.
- **Detalhamento dos resultados:** apresenta critérios encontrados, critérios ausentes e trechos do currículo que justificam a identificação.
- **Organização:** permite ordenar candidatos por pontuação ou nome e ocultar aqueles que não atendem aos requisitos.
- **Exportação CSV:** possibilita exportar os resultados da triagem para análise em planilhas.
- **Persistência local:** salva as configurações dos critérios no armazenamento local do navegador.

## 🛠️ Tecnologias utilizadas

| Tecnologia | Finalidade |
|---|---|
| HTML5 | Estrutura da aplicação |
| CSS3 | Estilização e interface responsiva |
| JavaScript | Lógica e processamento da aplicação |
| PDF.js | Extração de texto de arquivos PDF |
| Mammoth.js | Leitura de documentos DOCX |
| Tesseract.js | Reconhecimento óptico de caracteres (OCR) |
| LocalStorage | Armazenamento local das configurações |

## 🚀 Como utilizar

1. Abra a aplicação em um navegador moderno.
2. Configure o perfil da vaga:
   - Adicione os requisitos obrigatórios.
   - Adicione os requisitos desejáveis.
   - Defina a experiência mínima, se necessário.
   - Selecione a formação mínima.
   - Informe a cidade ou região, caso seja relevante.
3. Arraste os currículos para a área de upload ou clique para selecionar os arquivos.
4. Aguarde o processamento dos documentos.
5. Analise a pontuação e a classificação de cada candidato.
6. Clique em um candidato para visualizar os detalhes da análise.
7. Utilize a opção **Exportar CSV** para salvar os resultados.

## 📊 Como funciona a pontuação?

A aplicação utiliza uma pontuação ponderada, considerando os critérios configurados para a vaga.

| Critério | Peso |
|---|---:|
| Requisitos obrigatórios | 50 |
| Requisitos desejáveis | 25 |
| Experiência profissional | 15 |
| Formação acadêmica | 10 |
| Localização | 10 |

Os pesos são normalizados de acordo com os critérios preenchidos. Dessa forma, critérios não configurados não entram no cálculo.

**Importante:** a ausência de um requisito obrigatório faz com que o candidato seja classificado como "Não atende", independentemente da pontuação obtida.

## 🔒 Privacidade

A privacidade dos dados é uma das características centrais do projeto.

- Os currículos são processados diretamente no navegador.
- Os arquivos não são enviados para um servidor da aplicação.
- As configurações dos critérios são armazenadas localmente no navegador.
- A extração de texto e o reconhecimento OCR acontecem no ambiente do usuário.

**Observação:** a aplicação utiliza bibliotecas externas carregadas por CDN, portanto necessita de conexão com a internet para carregar esses recursos. Os arquivos dos currículos, entretanto, são processados localmente.

## 📱 Interface

A aplicação possui uma interface responsiva, com layout adaptável para diferentes tamanhos de tela, permitindo sua utilização tanto em computadores quanto em dispositivos móveis.

## ⚠️ Limitações

- A identificação de competências é baseada na busca textual e em um conjunto de sinônimos predefinidos, não em inteligência artificial semântica.
- Informações de experiência e formação são estimadas a partir de padrões encontrados no texto.
- A identificação de nomes e contatos depende da estrutura e da qualidade do currículo.
- Documentos digitalizados podem apresentar resultados de OCR imprecisos.
- A pontuação representa uma correspondência textual com os critérios definidos, não uma avaliação definitiva da qualificação profissional.

## 🎯 Objetivo

O objetivo do projeto é tornar a triagem inicial de currículos mais rápida, organizada e transparente, oferecendo uma ferramenta prática para comparar candidatos com os requisitos de uma oportunidade profissional.

---

**Triagem de Currículos**  
*Uma ferramenta simples e eficiente para organizar processos seletivos.*
