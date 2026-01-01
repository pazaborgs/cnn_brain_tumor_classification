
# 🧠 Classificação de Tumores Cerebrais com Deep Learning (CNNs)

## *Brain Tumor**

Este trabalho apresenta o desenvolvimento e a avaliação de modelos baseados em Redes Neurais Convolucionais (CNNs) para a classificação automática de tumores cerebrais em imagens de ressonância magnética (RM). Considerando a alta taxa de mortalidade associada aos tumores do Sistema Nervoso Central, a detecção precoce e precisa é fundamental para o sucesso do tratamento.

O projeto foi desenvolvido como Trabalho de Conclusão de Curso (TCC) do curso de Ciência de Dados da Universidade Virtual do Estado de São Paulo (UNIVESP), com o objetivo de testar e comparar diferentes abordagens de Deep Learning em um problema de diagnóstico médico por imagem.

## 🩻 Modelos e Metodologias

Foram implementadas duas redes neurais:

1. Uma CNN com arquitetura personalizada, desenvolvida do zero.

2. Uma CNN usando Transfer Learning, utilizando a arquitetura InceptionV3 como backbone.

## 📊 Base de Dados

Para alcançar os objetivos propostos, foi utilizada a base de dados Brain Tumor Classification (MRI), disponível no site Kaggle, compartilhada pelo usuário Sartaj. O Kaggle é uma plataforma para cientistas de dados, especialistas em aprendizado de máquina e estudantes, onde os usuários podem competir entre si na criação de modelos robustos de aprendizado de máquina. Também funciona como um grande repositório de conjuntos de dados com enfoque em ciência de dados.

Este dataset é composto por imagens de ressonâncias magnéticas cerebrais, categorizadas nas classes Glioma, Meningioma, Pituitário ou ausência de tumor. O dataset contém um total de 3264 imagens em formato. jpg, com variações de tamanho e predominância de tons de cinza.

[🎲 Link para o Dataset](https://www.kaggle.com/datasets/sartajbhuvaji/brain-tumor-classification-mri)

## 🛠️ Tecnologias Utilizadas

-   **Linguagem**: Python
-   **Frameworks**:  TensorFlow, Keras
-   **Manipulação de Dados**: Pandas, NumPy
-   **Visualização**:  Matplotlib, Seaborn, Scikit-learn
-   **Ambiente**: Google Colab

## 📊 Resumo dos Resultados

Abaixo, um resumo das métricas obtidas nos testes (conjunto de teste isolado de 10%):

| Modelo  | F1-Score (Macro) | Observação Principal |  
| :---  |:---: | :--- |  
| CNN Personalizada | 0.77 | Dificuldade em distinguir Meningiomas (Recall baixo na classe 2). |  
| InceptionV3| 0.88| Superou o gargalo da classe Meningioma e apresentou alta generalização. |

## ⚠️ Limitações do Trabalho

Embora os resultados sejam promissores, este projeto acadêmico possui limitações que foram mapeadas para futuras iterações (baseado no feedback da banca):

-   **Validação Estatística**: A comparação atual baseia-se em métricas diretas. Uma validação mais robusta (ex. Cross-Validation K-Fold e Testes de Hipótese) é necessária para confirmar a significância estatística da superioridade do InceptionV3.
-   **Análise de Erros**: Persiste uma confusão visual entre Gliomas e Meningiomas. Uma investigação radiológica mais profunda ou uso de Explainable AI (ex. Grad-CAM) podem ser capazes de explicar essa dificuldade intrínseca nos dados.
-   **Dataset**: O uso de uma base pública desbalanceada e limitada não reflete totalmente a variabilidade de equipamentos encontrados em ambiente clínico real.

## 🚀 Como Executar

O projeto foi desenvolvido inteiramente no Google Colab.

1.  Acesse o notebook: [Clicando aqui](https://colab.research.google.com/drive/1hy-yDlLAtCa2x9roaotL9Kk6A3dQrZuP#scrollTo=klLW2P3snTxU).
2.  Faça uma cópia para o seu Drive (`Arquivo > Salvar uma cópia no Drive`).
3.  O notebook baixa o dataset diretamente, mas será necessário fornecer o arquivo `kaggle.json` (token de API) disponível no kaggle.
  
Para obter o `kaggle.json`:

1. Acesse sua conta no Kaggle e navegue até Account (Conta) -> Settings (Configurações)
2. Role até a seção "API", clique em "Create New API Token" (Criar Novo Token de API).
3. O arquivo kaggle.json será automaticamente baixado para o seu computador. Este arquivo contém suas credenciais e deve ser mantido privado. Use-o para rodar o notebook.

## 👨‍💻 Autores

Trabalho desenvolvido como requisito para obtenção do título de Bacharel em Ciência de Dados pela UNIVESP (2025).

-   Patrick Regis (e grupo)
-   Orientador:  Darwish Ahmad Herati

---

Este projeto é para fins educacionais e acadêmicos. Não deve ser utilizado como ferramenta de diagnóstico médico real sem validação clínica apropriada.

[👉🏽 Desenvolvedor do Código](www.linkedin.com/in/patrickrgsanjos)

