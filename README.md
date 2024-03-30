# Microsoft Azure AI Fundamentals

Bootcamp da DIO em parceria com a Microsoft, visando a preparação de profissionais para a certificação AI-900.

## Projeto 3: Análise de Sentimentos com Language Studio no Azure AI

Neste terceiro desafio de projeto, o objetivo é utilizar as ferramentas de reconhecimento de fala e análise de sentimentos na plataforma Language Studio. 

## Etapas de Projeto

### 1. Speech Studio

Ao acessar o Speech Studio (https://speech.microsoft.com), acesse o ícone de configurações (Settings) e clique em "Create a new resource".
![01](https://github.com/mkatzor36/dioBootcampAI900_projeto3/assets/54877987/e587e62b-b929-45a0-aa6f-c1d08c76d744)
![02](https://github.com/mkatzor36/dioBootcampAI900_projeto3/assets/54877987/8cd405ee-93ab-4314-8d02-46228a8c74fe)

Entre com os dados para criar um novo recurso e clique em "Create resource". Após isso, selecione-o e clique em "Use resource".
![03](https://github.com/mkatzor36/dioBootcampAI900_projeto3/assets/54877987/85b983b3-3e7a-48b3-aabe-537c840829a4)
![04](https://github.com/mkatzor36/dioBootcampAI900_projeto3/assets/54877987/1e1f03f0-d687-4d76-b92b-7bcb40c3eb22)

Selecione a ferramenta "Real-time speech to text" da aba "Speech to text".
![05](https://github.com/mkatzor36/dioBootcampAI900_projeto3/assets/54877987/917125ed-35c1-4951-b41b-5a33d7c75e20)

Ao acessar a ferramenta, selecione o idioma de preferência (no caso, foi selecionado Português Brasileiro) e faça o upload do arquivo de áudio a ser analisado. O arquivo JSON está disponível na pasta *outputs*.
![06](https://github.com/mkatzor36/dioBootcampAI900_projeto3/assets/54877987/542362cd-5c63-48ed-9c72-420c3162fe64)

Uma possibilidade de aplicação desse recurso consiste em transcrever conteúdos educacionais (como vídeo-aulas) que não estejam disponíveis em um idioma que a pessoa compreenda. Em conjunto com uma ferramenta de tradução, isso pode ampliar o acesso educacional em diferentes áreas.

### 2. Language Studio

Ao acessar o portal do Azure, vá em "Create a resource" e procure pelo serviço de linguagem na categoria "AI + Machine Learning". 
![07](https://github.com/mkatzor36/dioBootcampAI900_projeto3/assets/54877987/66e20663-a61e-4e22-b819-50ed3de4f4b0)

Insira os dados do novo recurso e selecione a opção "Free F0" em "Pricing tier". Espere a conclusão do deployment.
![08](https://github.com/mkatzor36/dioBootcampAI900_projeto3/assets/54877987/ddc72f5b-6659-4206-84e1-6ced5cbb0b1c)
![09](https://github.com/mkatzor36/dioBootcampAI900_projeto3/assets/54877987/91c4c5b3-cf26-488c-953d-ec9db34bb11f)

No Language Studio (https://language.cognitive.azure.com/), crie o recurso para acessar as ferramentas.
![10](https://github.com/mkatzor36/dioBootcampAI900_projeto3/assets/54877987/200e9361-ca9c-4514-93dd-89dd793d3c86)

Selecione a ferramenta "Analyze sentiment and mine opinions" da aba "Classify text".
![11](https://github.com/mkatzor36/dioBootcampAI900_projeto3/assets/54877987/0ddb171c-7067-4f63-9e9c-48c25583db9d)

Uma possibilidade de aplicação dessa ferramenta é a análise de artigos científicos. Ao analisar o resumo e/ou a conclusão, o modelo poderia retornar se os resultados do estudo foram positivos ou negativos, permitindo ao pesquisador classificar os artigos conforme os seus resultados, otimizando as etapas de pesquisa de referências e de revisão da literatura de trabalhos acadêmicos. Para o seguinte teste, foi utilizado o arquivo *languageStudioTest1-EN.txt*, que contém o resumo de um artigo da revista Progress in Chemistry.
![12](https://github.com/mkatzor36/dioBootcampAI900_projeto3/assets/54877987/f4bf979a-4db8-42f3-8037-fa1cc549b602)

Os resultados da análise do modelo estão disponíveis abaixo. O arquivo JSON dos resultados está disponível na pasta *outputs*.
![13](https://github.com/mkatzor36/dioBootcampAI900_projeto3/assets/54877987/aaf15703-7941-4181-9c70-699a3aa27f33)

| Sentence | Positive (%) | Neutral (%) | Negative (%) |
|---|---|---|---|
| 1 | 57 | 41 | 2 |
| 2 | 1 | 99 | 1 |
| 3 | 1 | 98 | 1 |
| 4 | 14 | 85 | 1 |
| 5 | 2 | 97 | 1 |
| 6 | 1 | 99 | 0 |
| 7 | 2 | 98 | 1 |
| 8 | 0 | 98 | 1 |
| 9 | 9 | 90 | 1 |
| 10 | 1 | 98 | 1 |
| 11 | 2 | 96 | 1 |

Em seguida, foi realizado a análise do resumo no idioma original do artigo, utilizando o arquivo *languageStudioTest1-CN.txt*.
![14](https://github.com/mkatzor36/dioBootcampAI900_projeto3/assets/54877987/d23c3ca5-f225-47c0-9124-fa62d53edda7)

Os idiomas da análise do modelo estão disponíveis abaixo. O idioma detectado foi o Chinês Simplificado. O arquivo JSON dos resultados está disponível na pasta *outputs*.
![15](https://github.com/mkatzor36/dioBootcampAI900_projeto3/assets/54877987/2d658f4a-0bef-4021-9dfb-37a8fa3186cc)

| Sentence | Positive (%) | Neutral (%) | Negative (%) |
|---|---|---|---|
| 1 | 79 | 20 | 1 |
| 2 | 0 | 100 | 0 |
| 3 | 0 | 100 | 0 |
| 4 | 0 | 97 | 2 |
| 5 | 3 | 97 | 0 |
| 6 | 1 | 99 | 0 |
| 7 | 0 | 100 | 0 |

### sss

### sss

A ferramenta de tradução do Azure pode ser utilizada para ampliar bases de dados e facilitar o acesso de conteúdo científico, ao traduzir artigos que não estejam disponíveis no idioma do leitor e/ou em inglês.

## Referências

1. https://aka.ms/ai900-speech;
2. https://aka.ms/ai900-text-analysis;
3. Jianguo, L. *et al.* **Nano-Hydroxyapatite/Polymer Composite as Bone Repair Materials.** Progress in Chemistry, Vol. 27, 2015. *Disponível em:* https://manu56.magtech.com.cn/progchem/EN/abstract/abstract11484.shtml;
