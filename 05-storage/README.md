# 💾 Azure Storage

![Status](https://img.shields.io/badge/AZ--900-Concluído-success)
![Platform](https://img.shields.io/badge/Microsoft-Azure-0078D4)
![Module](https://img.shields.io/badge/Módulo-Armazenamento-blue)

![Azure Labs](../assets/banner.png)

## 🎯 Objetivo

Neste módulo foram estudados os principais serviços de armazenamento do Microsoft Azure, entendendo como as contas de armazenamento organizam os dados e como diferentes opções de redundância, transferência e migração podem ser utilizadas de acordo com cada cenário.

---

## 📚 Serviços de armazenamento estudados

### Storage Account

A **Azure Storage Account** é o recurso utilizado para disponibilizar os serviços de armazenamento do Azure.

Uma conta de armazenamento pode disponibilizar diferentes tipos de armazenamento, como:

- Blob Storage
- Azure Files
- Queue Storage
- Table Storage

A configuração de redundância é definida na conta de armazenamento e é compartilhada pelos serviços de armazenamento associados a ela. :contentReference[oaicite:0]{index=0}

---

## 🗂️ Tipos de armazenamento

### Blob Storage

O **Azure Blob Storage** é utilizado para armazenar grandes quantidades de dados não estruturados.

Exemplos:

- Imagens
- Vídeos
- Documentos
- Backups
- Logs
- Arquivos de aplicação

---

### Azure Files

O **Azure Files** fornece compartilhamentos de arquivos gerenciados pelo Azure.

Pode ser utilizado em cenários nos quais aplicações ou usuários precisam acessar arquivos compartilhados.

---

### Queue Storage

O **Queue Storage** permite armazenar mensagens para comunicação assíncrona entre componentes de aplicações.

Um exemplo seria uma aplicação que coloca tarefas em uma fila para serem processadas posteriormente.

---

### Table Storage

O **Table Storage** fornece armazenamento NoSQL para dados estruturados em formato de tabelas.

É adequado para determinados cenários que precisam armazenar grandes quantidades de dados estruturados sem utilizar um banco de dados relacional tradicional.

---

## 🗄️ Camadas de armazenamento

O Azure Blob Storage possui diferentes camadas de acesso que permitem equilibrar custo e frequência de acesso aos dados.

| Camada | Utilização |
|---|---|
| **Hot** | Dados acessados frequentemente |
| **Cool** | Dados acessados com menor frequência |
| **Cold** | Dados acessados raramente |
| **Archive** | Dados que precisam ser armazenados por longos períodos e raramente acessados |

A escolha da camada deve considerar principalmente a frequência de acesso e o custo de armazenamento e recuperação.

---

## 🔄 Redundância

O Azure Storage mantém múltiplas cópias dos dados para aumentar a durabilidade e protegê-los contra falhas de hardware, rede, energia e outros eventos. :contentReference[oaicite:1]{index=1}

### LRS — Locally Redundant Storage

Mantém cópias dos dados dentro de um único datacenter na região primária.

**Indicado quando:**

- O custo precisa ser reduzido;
- A proteção contra falhas dentro do datacenter é suficiente;
- Não existe necessidade de proteção contra uma falha regional.

---

### ZRS — Zone-Redundant Storage

Replica os dados de forma síncrona entre zonas de disponibilidade na região primária. :contentReference[oaicite:2]{index=2}

**Indicado quando:**

- É necessária maior disponibilidade;
- A aplicação precisa continuar funcionando mesmo com a indisponibilidade de uma zona.

---

### GRS — Geo-Redundant Storage

Mantém a redundância na região primária e replica os dados de forma assíncrona para uma região secundária geograficamente distante. :contentReference[oaicite:3]{index=3}

**Indicado para:**

- Recuperação de desastres;
- Proteção contra indisponibilidade regional.

---

### GZRS — Geo-Zone-Redundant Storage

Combina redundância entre zonas na região primária com replicação para uma região secundária. :contentReference[oaicite:4]{index=4}

É uma opção para cenários que precisam combinar alta disponibilidade na região primária e proteção contra falhas regionais.

---

### Comparação

```text
                    REGIÃO PRIMÁRIA
                         │
          ┌──────────────┼──────────────┐
          │              │              │
         LRS            ZRS            GRS/GZRS
          │              │              │
     1 datacenter    Várias zonas    Região secundária
                                         │
                                         ▼
                                  Proteção regional
