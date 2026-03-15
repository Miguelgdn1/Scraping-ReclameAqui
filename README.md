# 🎰 Scraper Reclame Aqui — Casas de Aposta 🕷️

> [!NOTE]
> Script de automação para extração de dados de empresas da categoria **"Casa de Aposta"** no Reclame Aqui.
> Coleta métricas de reputação e exporta os resultados em planilha Excel.

<table>
  <tr>
    <td width="800px">
      <div align="justify">
        Este projeto automatiza a navegação no site <b>Reclame Aqui</b> para extrair dados da categoria <i>"Casa de Aposta"</i>. Utilizando <b>Selenium</b> para automação do navegador e <b>Beautiful Soup</b> para parsing do HTML, o script coleta as empresas classificadas como <i>"Melhores"</i> e <i>"Piores"</i>, extraindo métricas como nota, reclamações respondidas, índice de solução e percentual de clientes que voltariam a fazer negócio. Os dados são organizados e exportados automaticamente em uma <b>planilha Excel</b> para análise.
      </div>
    </td>
    <td>
      <div align="center">
        <img src="https://joaopauloaramuni.github.io/image/aramunilogo.png" alt="Logo do Projeto" width="120px"/>
       
      </div>
    </td>
  </tr>
</table>

---

## 🚧 Status do Projeto

[![Versão](https://img.shields.io/badge/Versão-v1.0.0-blue?style=for-the-badge)](https://github.com/seu-usuario/scraper-reclame-aqui/releases)
![Python](https://img.shields.io/badge/Python-3.x-007ec6?style=for-the-badge&logo=python&logoColor=white)
![Selenium](https://img.shields.io/badge/Selenium-4.x-007ec6?style=for-the-badge&logo=selenium&logoColor=white)
![Pandas](https://img.shields.io/badge/Pandas-2.x-007ec6?style=for-the-badge&logo=pandas&logoColor=white)
![GitHub license](https://img.shields.io/github/license/seu-usuario/scraper-reclame-aqui?style=for-the-badge&color=007ec6&logo=opensourceinitiative)
![GitHub last commit](https://img.shields.io/github/last-commit/seu-usuario/scraper-reclame-aqui?style=for-the-badge&logo=clockify)

---

## 📚 Índice
- [Sobre o Projeto](#-sobre-o-projeto)
- [Funcionalidades Principais](#-funcionalidades-principais)
- [Tecnologias Utilizadas](#-tecnologias-utilizadas)
- [Instalação e Execução](#-instalação-e-execução)
  - [Pré-requisitos](#pré-requisitos)
  - [Instalação de Dependências](#-instalação-de-dependências)
  - [Como Executar](#-como-executar)
- [Estrutura de Pastas](#-estrutura-de-pastas)
- [Demonstração](#-demonstração)
- [Documentações Utilizadas](#-documentações-utilizadas)
- [Autores](#-autores)
- [Contribuição](#-contribuição)
- [Licença](#-licença)

---

## 📝 Sobre o Projeto

O **Scraper Reclame Aqui** surgiu da necessidade de monitorar e comparar a reputação de empresas do segmento de **Casas de Aposta** de forma automatizada e estruturada.

O Reclame Aqui é a principal plataforma brasileira de avaliações e reclamações de consumidores, e seus dados refletem diretamente a qualidade do atendimento e a confiabilidade das empresas. Contudo, coletar essas informações manualmente é inviável em escala.

Este projeto resolve esse problema ao:

- **Automatizar** a navegação e coleta de dados do site, sem intervenção humana.
- **Estruturar** os dados em um formato tabular e exportável.
- **Facilitar** análises comparativas entre as melhores e piores empresas do setor.

Pode ser utilizado por analistas de mercado, jornalistas de dados, pesquisadores ou qualquer pessoa que queira acompanhar a reputação de Casas de Aposta no Brasil.

> [!NOTE]
> Este projeto tem fins informativos e educacionais. Verifique os Termos de Uso do Reclame Aqui antes de utilizar em produção.

---

## ✨ Funcionalidades Principais

- 🏆 **Coleta de Melhores Empresas:** Extrai automaticamente a lista de empresas mais bem avaliadas na categoria "Casa de Aposta".
- 💀 **Coleta de Piores Empresas:** Extrai automaticamente a lista de empresas com piores avaliações.
- 📊 **Extração de Métricas:** Para cada empresa, coleta as seguintes métricas de reputação:
  - **Nota geral** da empresa no Reclame Aqui.
  - **Reclamações respondidas (%):** Percentual de reclamações com retorno da empresa.
  - **Voltariam a fazer negócio (%):** Percentual de clientes satisfeitos.
  - **Índice de solução (%):** Percentual de problemas efetivamente resolvidos.
- 📁 **Exportação para Excel:** Todos os dados coletados são salvos automaticamente em uma planilha `.xlsx`.

---

## 🛠 Tecnologias Utilizadas

### 🐍 Linguagem

* **Python 3.x** — Linguagem principal do projeto.

### 📦 Bibliotecas e Frameworks

| Biblioteca | Versão | Finalidade |
| :--- | :---: | :--- |
| `selenium` | 4.x | Automação do navegador Chrome para navegação dinâmica no site. |
| `beautifulsoup4` | 4.x | Parsing e extração de dados do HTML retornado pelo navegador. |
| `pandas` | 2.x | Manipulação e estruturação dos dados em tabela. |
| `openpyxl` | 3.x | Escrita e formatação do arquivo Excel de saída. |

### ⚙️ Ferramentas Externas

* **Google Chrome** — Navegador utilizado pelo Selenium para automação.
* **ChromeDriver** — Driver que conecta o Selenium ao Chrome. Deve ser compatível com a versão do Chrome instalada e estar no `PATH` do sistema.

---

## 🔧 Instalação e Execução

### Pré-requisitos

Certifique-se de ter o seguinte instalado em seu ambiente:

* **Python 3.x** — [Download oficial](https://www.python.org/downloads/)
* **Google Chrome** — [Download oficial](https://www.google.com/chrome/)
* **ChromeDriver** — Versão compatível com o seu Chrome. Disponível em [chromedriver.chromium.org](https://chromedriver.chromium.org/downloads) ou via [chrome-for-testing](https://googlechromelabs.github.io/chrome-for-testing/).

> [!IMPORTANT]
> O ChromeDriver precisa estar no `PATH` do sistema ou no mesmo diretório do script para que o Selenium consiga utilizá-lo.

---

### 📦 Instalação de Dependências

1. **Clone o repositório:**

```bash
git clone https://github.com/seu-usuario/scraper-reclame-aqui.git
cd scraper-reclame-aqui
```

2. **(Opcional, mas recomendado) Crie e ative um ambiente virtual:**

```bash
# Criar o ambiente virtual
python -m venv venv

# Ativar no Linux/macOS
source venv/bin/activate

# Ativar no Windows
venv\Scripts\activate
```

3. **Instale as dependências a partir do `requirements.txt`:**

```bash
pip install -r requirements.txt
```

O arquivo `requirements.txt` contém:

```txt
selenium
beautifulsoup4
pandas
openpyxl
```

---

### ⚡ Como Executar

Com as dependências instaladas e o ChromeDriver configurado no `PATH`, execute:

```bash
python main.py
```

O script irá:
1. Abrir o Chrome automaticamente.
2. Navegar até a página de "Casas de Aposta" no Reclame Aqui.
3. Extrair os dados das empresas classificadas como "Melhores" e "Piores".
4. Salvar os dados no arquivo **`casas_de_aposta.xlsx`** no diretório do projeto.

---

## 📂 Estrutura de Pastas

```
.
├── src
   ├── main.py                 # 🚀 Script principal — ponto de entrada da aplicação.
   ├── scraper_pack
        ├── ReclameAquiScraper.py     # 🚀 Fluxo principal — onde tudo acontece.
        ├── ExportadorExcel.py        # 🚀 Salva as informações buscadas em uma planilha.
├── requirements.txt         # 📦 Dependências do projeto.
├── casas_de_aposta.xlsx     # 📊 Planilha gerada após a execução (não versionada).
├── .gitignore               # 🧹 Ignora arquivos gerados e ambiente virtual.
└── README.md                # 📘 Documentação do projeto.
```

> [!NOTE]
> O arquivo `casas_de_aposta.xlsx` é gerado em tempo de execução e não deve ser versionado. Adicione-o ao `.gitignore` se necessário.

---

## 🎥 Demonstração

### 💻 Exemplo de Saída no Terminal

Ao executar o script, a saída esperada no terminal é semelhante a:

```bash
python main.py
```

```text
[INFO] Iniciando o navegador Chrome...
[INFO] Acessando Reclame Aqui — Categoria: Casa de Aposta...
[INFO] Coletando dados das Melhores empresas...
[SUCCESS] 10 empresas encontradas na categoria "Melhores".
[INFO] Coletando dados das Piores empresas...
[SUCCESS] 10 empresas encontradas na categoria "Piores".
[INFO] Exportando dados para casas_de_aposta.xlsx...
[SUCCESS] Arquivo salvo com sucesso: casas_de_aposta.xlsx
Tempo de execução: 18.42s
```

### 📊 Exemplo de Saída na Planilha Excel

O arquivo `casas_de_aposta.xlsx` gerado terá o seguinte formato:

| Empresa | Classificação | Nota | Reclamações Respondidas (%) | Voltariam a Fazer Negócio (%) | Índice de Solução (%) |
|---|---|---|---|---|---|
| Empresa A | Melhor | 8.5 | 95% | 82% | 88% |
| Empresa B | Melhor | 7.9 | 91% | 74% | 79% |
| Empresa X | Pior | 3.1 | 42% | 18% | 31% |
| Empresa Y | Pior | 2.8 | 37% | 12% | 25% |

---

## 🔗 Documentações Utilizadas

* 📖 **Selenium:** [Documentação Oficial do Selenium para Python](https://selenium-python.readthedocs.io/)
* 📖 **Beautiful Soup:** [Documentação Oficial do Beautiful Soup 4](https://www.crummy.com/software/BeautifulSoup/bs4/doc/)
* 📖 **Pandas:** [Documentação Oficial do Pandas](https://pandas.pydata.org/docs/)
* 📖 **OpenPyXL:** [Documentação Oficial do OpenPyXL](https://openpyxl.readthedocs.io/en/stable/)
* 📖 **ChromeDriver:** [ChromeDriver — WebDriver for Chrome](https://chromedriver.chromium.org/)
* 📖 **Reclame Aqui:** [Reclame Aqui — Categoria Casa de Aposta](https://www.reclameaqui.com.br/)

---

## 🤝 Contribuição

1. Faça um `fork` do projeto.
2. Crie uma branch para sua feature (`git checkout -b feature/minha-feature`).
3. Commit suas mudanças (`git commit -m 'feat: Adiciona nova funcionalidade X'`). **(Utilize [Conventional Commits](https://www.conventionalcommits.org/en/v1.0.0/))**
4. Faça o `push` para a branch (`git push origin feature/minha-feature`).
5. Abra um **Pull Request (PR)**.

---

## 📄 Licença

Este projeto é distribuído sob a **[Licença MIT](./LICENSE)**.

---
