# ETL & Data Warehouse — Materiais de Aula

Repositório mantido por **Jefferson Rodrigo Speck** com notebooks e exemplos práticos sobre **ETL** e **Data Warehouse (DW)**.
O conteúdo é **aberto**: você pode usar e modificar livremente, **citando a fonte** (ver [Licença](#licença)).

---

## Estrutura do Repositório

```
/
├─ aprendizado/   # materiais básicos de Python
│  ├─ 1 - Iniciando_Python.ipynb
│  ├─ 2 - Types.ipynb
│  ├─ 3 - Expressions_Variables.ipynb
│  ├─ 4 - Strings.ipynb
│  ├─ 5 - Atividade.ipynb
│  ├─ 6 - Lists.ipynb
│  ├─ 7 - Tuples.ipynb
│  ├─ 8 - Atividade.ipynb
│  ├─ 9 - Conditions.ipynb
│  ├─ 10 - Loops.ipynb
│  ├─ 11 - Functions.ipynb
│  └─ 12 - Classes.ipynb
├─ DW_aula_01.ipynb   # primeira aula sobre ETL e mini DW
├─ data/
│  ├─ raw/            # dados brutos (landing zone)
│  └─ curated/        # dados tratados (CSV/Parquet)
├─ outputs/           # bancos SQLite, gráficos, relatórios
└─ README.md
```

---

## Conteúdo

### Aprendizado (Python básico)

* Introdução à linguagem Python
* Variáveis, tipos de dados e operadores
* Estruturas condicionais e de repetição
* Funções e boas práticas iniciais

### ETL & Data Warehouse

* **Aula 01** — ETL + Mini DW usando a [DummyJSON API](https://dummyjson.com)
  Notebook: `DW_aula_01.ipynb`
* Próximas aulas seguirão o padrão:
  `DW_aula_02.ipynb`, `DW_aula_03.ipynb`, etc.

---

## Instalação do Python

### Windows

**Opção A — via Microsoft Store / winget (recomendado):**

```powershell
winget install Python.Python.3
python --version
pip --version
```

**Opção B — instalador oficial:**

1. Baixe em: [python.org/downloads/windows](https://www.python.org/downloads/windows/)
2. Execute o instalador e **marque** “Add Python to PATH”.
3. Verifique:

   ```powershell
   python --version
   pip --version
   ```

> Se o PowerShell bloquear scripts:
> `Set-ExecutionPolicy -Scope CurrentUser RemoteSigned -Force`

### Linux (Debian/Ubuntu)

```bash
sudo apt update
sudo apt install -y python3 python3-pip python3-venv
python3 --version
pip3 --version
```

(Para Fedora/Arch, veja instruções específicas acima)

---

## Preparar o ambiente

1. **Clonar o repositório**

   ```bash
   git clone <URL-do-repositorio>
   cd <pasta-do-repositorio>
   ```

2. **Criar e ativar ambiente virtual**

   * Windows:

     ```powershell
     python -m venv .venv
     .\.venv\Scripts\Activate.ps1
     ```
   * Linux:

     ```bash
     python3 -m venv .venv
     source .venv/bin/activate
     ```

3. **Instalar dependências**

   * Se houver `requirements.txt`:

     ```bash
     pip install -r requirements.txt
     ```
   * Caso contrário (pacotes usados nas aulas):

     ```bash
     pip install requests pandas pyarrow matplotlib jupyterlab
     ```

4. **Abrir os notebooks**

   ```bash
   jupyter lab
   # ou
   jupyter notebook
   ```

---

## Licença

Você tem **permissão para usar, copiar, modificar e distribuir** este conteúdo, inclusive para fins acadêmicos e comerciais, **desde que credite a autoria** como:

> **Jefferson Rodrigo Speck**

Exemplo de citação:

> “Baseado em materiais de ETL & Data Warehouse de Jefferson Rodrigo Speck.”

---

## Contribuições

* Relate problemas e ideias em **Issues**
* Sugira melhorias via **Pull Requests**
* Feedbacks e colaborações são bem-vindos!

