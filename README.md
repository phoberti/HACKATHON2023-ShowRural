# HACKATHON2023 – Sistema de Validação de Higienização

Projeto desenvolvido durante o Hackathon Show Rural 2023 pela equipe The Byte Busters.

Este repositório é um fork criado para documentar minha participação no desenvolvimento da solução proposta.



##  Desafio

Criar um mecanismo de controle que assegure que colaboradores de granjas realizem corretamente o protocolo de banho obrigatório, respeitando o direito à privacidade.

O principal risco sanitário abordado foi a contaminação por salmonela.



##  Solução Desenvolvida

A solução combina:

-  Reconhecimento facial via webcam
-  Captura e análise de áudio do chuveiro
-  Geração de histograma de amplitude sonora
-  Validação de permanência no ambiente

O sistema funciona da seguinte forma:

1. O colaborador é identificado por reconhecimento facial na entrada.
2. Caso um rosto autorizado seja detectado, o sistema inicia a captura de áudio.
3. O áudio do banho é gravado por 10 segundos.
4. Um histograma da amplitude sonora é gerado para análise.
5. O padrão sonoro pode ser comparado com um padrão esperado de banho real.



##  Estrutura do Projeto

### 🔹 main.py
Arquivo principal que integra:
- Validação facial
- Captura de áudio

### 🔹 facial.py
Responsável por:
- Carregar imagens de referência
- Extrair encodings faciais
- Capturar imagem da webcam
- Comparar distância facial (threshold 0.6)
- Validar presença do colaborador

Tecnologias utilizadas:
- OpenCV
- face_recognition

### 🔹 audio.py
Responsável por:
- Captura de áudio com PyAudio
- Armazenamento em WAV
- Leitura com scipy
- Geração de histograma com matplotlib

Tecnologias utilizadas:
- PyAudio
- NumPy
- SciPy
- Matplotlib



##  Tecnologias Utilizadas

- Python
- OpenCV
- face_recognition
- PyAudio
- NumPy
- SciPy
- Matplotlib



##  Objetivo Técnico

Criar um mecanismo de validação que:

- Identifique o colaborador sem invadir privacidade
- Verifique se houve permanência no local
- Analise o padrão sonoro do banho
- Minimize risco de fraude (água ligada sem pessoa presente)



##  Minha Participação

Projeto desenvolvido em equipe durante o hackathon. Contribuí no desenvolvimento da lógica de validação e integração entre reconhecimento facial e análise de áudio, além da estruturação da solução técnica proposta.

Este fork compõe meu portfólio como registro de participação em projeto prático envolvendo visão computacional e processamento de sinais.
