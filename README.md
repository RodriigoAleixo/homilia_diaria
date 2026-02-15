# 📜 Automação de Liturgia e Homilias

Este projeto é um script de automação em Python desenvolvido para coletar recursos católicos diários e enviá-los automaticamente via WhatsApp. Ele busca homilias de canais específicos no YouTube e, aos domingos, baixa o folheto litúrgico "O Povo de Deus" da Arquidiocese de Brasília.

## ✨ Funcionalidades

* **Busca de Homilias:** Localiza automaticamente os vídeos do dia dos canais:
* Padre Paulo Ricardo.
* Padre Mario Sartori.


* **Download de Folheto:** Identifica se o dia atual é domingo e realiza o download do PDF do folheto litúrgico diretamente do site da Arquidiocese de Brasília.
* **Integração com WhatsApp:** Envia os links das homilias encontradas para contatos ou grupos pré-definidos via WhatsApp Web.

## 🚀 Tecnologias Utilizadas

* **Python 3.x**
* **Selenium:** Automação de navegação web.
* **Requests:** Download de arquivos PDF.
* **Webdriver Manager:** Gerenciamento automático do driver do Chrome.

---

## 📋 Pré-requisitos

Antes de executar o script, você precisará instalar as dependências necessárias:

```bash
pip install selenium requests webdriver-manager

```

> **Nota:** É necessário ter o Google Chrome instalado em sua máquina.

---

## 🛠️ Como Usar

1. **Configuração de Grupos:**
No arquivo Python, localize a lista `grupos = ['Eu']` e substitua pelos nomes exatos dos seus contatos ou grupos do WhatsApp.
2. **Execução:**
Execute o script:
```bash
python nome_do_seu_arquivo.py

```


3. **Autenticação:**
O navegador abrirá no WhatsApp Web. Você terá **40 segundos** (conforme configurado no `time.sleep`) para escanear o QR Code com seu celular.
4. **Fluxo de Trabalho:**
O script irá:
* Verificar a data e o dia da semana.
* Acessar os canais do YouTube e capturar os links.
* Se for domingo, baixar o PDF na pasta raiz do projeto.
* Enviar as mensagens no WhatsApp.



---

## ⚠️ Observações Importantes

* **XPaths:** O código utiliza seletores XPath para encontrar botões e campos. Se os sites (Arquidiocese ou WhatsApp) mudarem o layout, esses caminhos podem precisar de atualização.
* **Tempo de Espera:** O script utiliza `time.sleep()`. Dependendo da velocidade da sua internet, pode ser necessário ajustar esses valores para garantir que as páginas carreguem totalmente.
* **Segurança:** Nunca compartilhe sua sessão do WhatsApp Web com terceiros e use a automação de forma responsável para evitar bloqueios na plataforma.

---

### 💡 Próximos Passos Sugeridos

* [ ] Implementar o envio do arquivo PDF baixado diretamente pelo WhatsApp.
* [ ] Utilizar `Headless mode` no Chrome para buscas que não exigem interação visual.
* [ ] Adicionar tratamento de exceções para dias em que o vídeo ainda não foi postado.

---
