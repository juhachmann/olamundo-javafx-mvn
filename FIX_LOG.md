
## Fixes

### Impressão de Relatório com JasperReport

- **Erro: incompatible type for field columnCount** 

Solução: No arquivo .jrxml correspondente havia um campo que estava sendo nomeado de 'COLUMN_7' e referenciava uma coluna de uma consulta em SQL (categoria.descrição). Alterei o mome do campo para 'categoria' e usei um alias de mesmo nome na query SQL declarada no mesmo arquivo. Após isto, o arquivo jrxml foi recompilado para .jasper usando o Jasper Studio. 

---

- **Erro: Font 'Arial' is not available to the JVM**

Solução: O erro só aparece em OS que não possuem a fonte Arial nativamente, como é o caso do Linux. Uma solução possível é instalar um pacote de fontes com

```
sudo apt-get install msttcorefonts
```

Referência: https://stackoverflow.com/questions/12425612/font-arial-is-not-available-to-the-jvm

---

- **Erros: relacionados a PDF, SingleSheet XLS e MultiSheet XLS**

Solução: Adicionar as dependências do JasperReport para PDF e Excel
