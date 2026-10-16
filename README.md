# Trabalho-6-Transformadas-de-Wavelet-Gabriel-e-Felipe
# Processamento Digital de Sinais - Práticas Avançadas
Este repositório contém implementações práticas e análises teóricas sobre técnicas fundamentais de Processamento Digital de Sinais (PDS), englobando multiplexação por divisão de código, análise multirresolução e filtragem adaptativa de ruído.

🛠️ Tecnologias Utilizadas
Python 3
NumPy & SciPy (Computação científica e álgebra linear)
PyWavelets (Transformada Wavelet discreta de múltiplos níveis)
Matplotlib (Visualização de dados e espectros)
📋 Conteúdo do Projeto
1. Multiplexação e De-multiplexação CDMA (Hadamard)
Simulação de um sistema de comunicação CDMA (Code Division Multiple Access) com  K=3  usuários ativos usando códigos ortogonais baseados na matriz de Hadamard ( L=8 ).

Codificação e Espectro: Demonstração visual de como a codificação espalha o espectro do sinal original de banda estreita.
Análise de Ruído: Avaliação do impacto de ruído AWGN na recepção.
Probabilidade de Erro ( Pe ): Comparação das curvas teóricas  Q(8/σ2−−−−√)  e simuladas de taxa de erro de bit (BER), analisando o cenário de código perfeito e o impacto de distorções no receptor (código imperfeito).
2. Análise de Sinais Não-Estacionários com Wavelets
Estudo de transições rápidas e transientes utilizando a Transformada Wavelet Discreta (DWT).

Wavelet Biorgonal (bior4.4): Decomposição em 5 níveis de aproximação (cA5) e detalhes (cD1 a cD5) para isolar componentes de alta frequência e descontinuidades localizadas no tempo.
Reconstrução Perfeita: Verificação prática do erro numérico de reconstrução ( ∥x−xr∥∞≈10−11 ).
3. Filtragem de Ruído (Denoising) no Sinal leleccum
Estudo de caso prático de atenuação de ruído de alta frequência com a Wavelet Daubechies 4 (db4).

Estimação de Ruído: Estimativa robusta do desvio padrão do ruído ( σ ) via desvio absoluto mediano (MAD) dos coeficientes do primeiro nível de detalhe (cD1).
Limiarização (Thresholding): Aplicação do limiar universal de Donoho-Johnstone (Soft e Hard Thresholding).
Wavelet vs. DFT: Comparação qualitativa e quantitativa (MSE) entre a filtragem baseada em limiarização de Wavelet e a filtragem tradicional baseada em limiar de amplitude na Transformada Discreta de Fourier (DFT).
📈 Resultados Principais
CDMA: A simulação comprovou com exatidão a curva teórica de erro e quantificou a perda de desempenho quando o receptor possui um código ligeiramente ruidoso ou desalinhado.
Denoising: O método Wavelet demonstrou melhor preservação de transientes abruptos do sinal leleccum em relação ao corte de frequências da DFT, minimizando o efeito de oscilação (fenômeno de Gibbs) nas bordas das transições.
