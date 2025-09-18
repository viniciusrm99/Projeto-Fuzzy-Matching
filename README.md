# Projeto: Fuzzy Matching de Produtos

Este projeto aplica **fuzzy matching** para padronizar nomes de produtos em uma base de vendas.  
Ele identifica variações de nomes (erros de digitação, abreviações ou acentuação diferente) e converte para um **produto padrão**, mantendo os valores originais quando a correspondência não é confiável.

---

## 1️⃣ Instalando as bibliotecas necessárias

```bash
# Para fuzzy matching
pip install rapidfuzz

# Para normalização de acentos e caracteres especiais
pip install Unidecode

```

## 2️⃣ Upload da base de dados

No Google Colab, você pode fazer upload do Excel diretamente:

```bash
from google.colab import files
import pandas as pd

# Fazendo upload do arquivo Excel
uploaded = files.upload()

# Lendo a planilha "base_vendas"
df_base = pd.read_excel("projeto_fuzzy_matching.xlsx", sheet_name="base_vendas")

# Conferindo as primeiras linhas
print(df_base.head())
```
