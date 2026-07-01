# 🩻 MedVision

Aplicação de Visão Computacional e Deep Learning para classificação automática de órgãos abdominais em imagens de CT scan, com IA Explicável (Grad-CAM) e interface interativa via Streamlit.

## 📌 Sobre o Projeto

O MedVision utiliza uma ResNet50 pré-treinada (transfer learning) para identificar órgãos abdominais em imagens de **tomografia computadorizada (CT scan)**. O modelo foi treinado com o dataset **OrganAMNIST** do MedMNIST, composto por ~34.000 imagens de cortes abdominais.

> ⚠️ **Limitação importante:** o modelo foi treinado exclusivamente com CT scans da região abdominal. Imagens de outras regiões (tórax, cabeça) ou outras modalidades (raio-x, ressonância magnética) podem gerar resultados incorretos.

## 🫁 Órgãos Classificados

| Classe | Órgão |
|---|---|
| bladder | Bexiga |
| femur-left | Fêmur esquerdo |
| femur-right | Fêmur direito |
| heart | Coração |
| kidney-left | Rim esquerdo |
| kidney-right | Rim direito |
| liver | Fígado |
| lung-left | Pulmão esquerdo |
| lung-right | Pulmão direito |
| pancreas | Pâncreas |
| spleen | Baço |

## 🚀 Como Rodar

**1. Clone o repositório:**
```bash
git clone https://github.com/ItzMvs/MedVision.git
cd MedVision
```

**2. Instale as dependências:**
```bash
pip install -r requirements.txt
```

**3. Rode o app:**
```bash
streamlit run app.py
```

## 🧠 Tecnologias

- Python 3.x
- PyTorch + ResNet50
- Streamlit
- Grad-CAM (IA Explicável)
- MedMNIST (OrganAMNIST)
- OpenCV

## 📂 Estrutura do Projeto
├── data/          # Dataset local (não incluído no repositório)
├── models/        # Pesos do modelo treinado (.pth)
├── src/
│   ├── app.py
│   ├── train.py
│   ├── model.py
│   ├── dataset.py
│   └── interpretability.py
└── README.md

## ⚡ Resultados

- **Acurácia de validação: 98.52%**
- **Val Loss: 0.0483**
- Épocas de treinamento: 5
