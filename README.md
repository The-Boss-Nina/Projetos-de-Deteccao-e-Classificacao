# Projetos de Detecção e Classificação

## Emotions Detection CNN

Este projeto é um programa que utiliza redes neurais convolucionais (CNNs) para detectar emoções em imagens. Ele emprega bibliotecas modernas de aprendizado de máquina e visão computacional para realizar a classificação das emoções presentes em rostos.

### Como Funciona

1. O modelo utiliza um dataset de imagens com rostos anotados para treinar uma CNN capaz de classificar emoções.
2. O script carrega o modelo treinado e aplica a detecção de emoções em novas imagens.
3. Os resultados são apresentados com as probabilidades para cada classe de emoção.

### Classes de Emoção
| Emoção          | Valor |
|-----------------|-------|
| Feliz           | 1     |
| Triste          | 2     |
| Neutro          | 3     |
| Bravo           | 4     |
| Surpreso        | 5     |
| Medo            | 6     |
| Nojo            | 7     |

### Requisitos

- **Bibliotecas Necessárias:**
  - Para instalar as dependências principais:
    ```bash
    pip install numpy
    pip install opencv-python
    pip install keras
    pip3 install --upgrade tensorflow
    pip install pillow
    ```
- **Outras Dependências:** Listadas no arquivo `requirements.txt`.

### Como Executar

1. **Prepare o Ambiente:**
   - Certifique-se de que todas as dependências listadas no arquivo `requirements.txt` estão instaladas.
     ```bash
     pip install -r requirements.txt
     ```

2. **Carregue o Modelo:**
   - O modelo treinado deve estar disponível nos arquivos `.h5` ou `.json`. Verifique o diretório do projeto.

3. **Execute o Script:**
   - Rode o script principal para iniciar a detecção:
     ```bash
     python main.py
     ```

### Banco de Dados

- [Kaggle LFWPeople](https://www.kaggle.com/datasets/atulanandjha/lfwpeople): Dataset utilizado para treinar ou validar o modelo.

---

## DeepFace

O DeepFace é um framework de aprendizado profundo voltado para reconhecimento facial e análise de emoções. Este projeto utiliza o DeepFace como base para realizar tarefas como verificação facial, análise de emoções e agrupamento de rostos similares.

### Funcionalidades Principais

1. **Reconhecimento Facial:**
   - Identifica rostos em imagens e vídeos.
2. **Análise de Emoções:**
   - Classifica as emoções exibidas nos rostos.
3. **Modelos Suportados:**
   - Suporta múltiplos modelos, como VGG-Face, Google FaceNet e OpenFace.

### Requisitos

- Instale o DeepFace e suas dependências:
  ```bash
  pip install deepface
  ```

### Como Executar

1. **Configuração:**
   - Certifique-se de que as dependências estão instaladas e o ambiente está configurado.
2. **Carregue e Analise Imagens:**
   - Execute os scripts para verificar emoções ou similaridade facial:
     ```python
     from deepface import DeepFace
     DeepFace.analyze(img_path="caminho_para_imagem")
     ```

### Referências

- [DeepFace GitHub Repository](https://github.com/serengil/deepface)

---

## Haarcascade

Este projeto utiliza o Haarcascade do OpenCV para realizar detecção de objetos, como rostos e olhos, em imagens e vídeos. Ele utiliza modelos pré-treinados baseados em cascatas para identificar padrões visuais em tempo real.

### Como Funciona

1. **Classificadores Haarcascade:**
   - Utiliza modelos pré-treinados como `haarcascade_frontalface_default.xml` para detecção de rostos.
2. **Análise em Tempo Real:**
   - Detecta e destaca rostos em vídeos capturados pela webcam ou em arquivos de vídeo pré-existentes.
3. **Ajustes Dinâmicos:**
   - Permite ajustar parâmetros, como escala e vizinhos mínimos, para personalizar a sensibilidade da detecção.

### Requisitos

- **Bibliotecas Necessárias:**
  - Instale o OpenCV:
    ```bash
    pip install opencv-python
    ```

### Como Executar

1. **Configure o Ambiente:**
   - Certifique-se de que os modelos Haarcascade estão disponíveis no diretório correto.
2. **Execute o Script:**
   - Use o OpenCV para carregar os classificadores e analisar imagens ou vídeos:
     ```python
     face_cascade = cv2.CascadeClassifier(cv2.data.haarcascades + "haarcascade_frontalface_default.xml")
     ```
3. **Resultados:**
   - Os resultados são exibidos com caixas delimitadoras ao redor dos objetos detectados.

### Referências

- [Documentação OpenCV](https://docs.opencv.org/3.1.0/d7/d8b/tutorial_py_face_detection.html#gsc.tab=0)