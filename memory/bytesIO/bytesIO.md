## 🔹 BytesIO – O que é?

`BytesIO` é uma classe do módulo `io` em Python que cria um **fluxo (buffer) de bytes em memória**, funcionando como um arquivo, mas armazenando os dados em RAM ao invés de no disco.

Em outras palavras, ele cria um **objeto de arquivo virtual para dados binários**, sendo útil quando:

- Precisamos trabalhar com arquivos binários (imagens, PDFs, zips) sem criar arquivos temporários.
- Manipulamos dados de upload ou download em APIs diretamente na memória.
- Queremos testar leitura/escrita de arquivos sem salvar no disco.
