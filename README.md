# Gerador de Certificados — CAEFEL

Gerador de certificados e declarações do **Centro Acadêmico de Engenharia Ferroviária e Logística (CAEFEL)**, da Faculdade de Engenharia Ferroviária e Logística — Instituto de Tecnologia (ITEC) — Universidade Federal do Pará (UFPA).

Aplicação em arquivo único (HTML, CSS e JavaScript). Os dados são preenchidos em um formulário e o documento é atualizado em tempo real ao lado, pronto para exportar em PDF ou imprimir.

## Modelos de documento

| Modelo | Título | Campos específicos |
|---|---|---|
| Participação em evento | CERTIFICADO | Nome da atividade/evento, carga horária, categoria de horas |
| Declaração de visita técnica | DECLARAÇÃO | RG do aluno, professor(a) e RG, disciplina, local, cidade/UF, carga horária (todos opcionais) |
| Membro do CAEFEL | CERTIFICADO | Cargo na gestão, carga horária, categoria de horas |
| Monitoria | CERTIFICADO | Disciplina, professor(a) orientador(a), período, carga horária |
| Minicurso | CERTIFICADO | Título, ministrante, data/período, carga horária, promotor |

O texto do corpo é montado automaticamente conforme o modelo escolhido e os campos preenchidos. Campos opcionais desmarcados são omitidos do texto. Todos os modelos aceitam geração em lote.

## Como usar

**Online (GitHub Pages):** acesse `https://sabazord.github.io/Certificado-Caefel/`, se o Pages estiver ativado.

**Local:** baixe o arquivo `index.html` e abra com duplo clique em qualquer navegador (Chrome, Edge ou Firefox). Não é preciso instalar nada.

1. Escolha o modelo de documento.
2. Preencha o nome do aluno e, se quiser, a matrícula.
3. Preencha os campos específicos do modelo e a data de emissão.
4. Preencha as três assinaturas (veja abaixo).
5. Clique em **Baixar PDF** ou **Imprimir**.

### Assinaturas

O documento tem três posições de assinatura (esquerda, centro e direita). Em cada uma é possível:

- preencher o nome de quem assina;
- enviar a imagem da assinatura (PNG, JPG ou WebP), que aparece sobre a linha;
- editar livremente o cargo que aparece abaixo da linha (uma quebra de linha no campo vira quebra de linha no documento);
- escolher um cargo pronto na lista (Diretor(a) da Faculdade, Presidente do CAEFEL, Coordenador(a) do Curso, Coordenador(a) do Evento, Professor(a) Orientador(a), Ministrante etc.) e ajustá-lo depois, se precisar;
- remover a assinatura do documento pelo botão ✕ e restaurá-la depois sem perder o nome.

Os cargos padrão são Diretor(a) da Faculdade, Vice-diretor(a) da Faculdade e Presidente do CAEFEL.

#### Assinatura em imagem

Ao enviar a imagem, o gerador remove automaticamente o fundo branco ou claro e corta as margens vazias. Assim, uma assinatura escaneada numa folha inteira fica do mesmo tamanho visual das demais. O nome digitado continua aparecendo abaixo da linha; se preferir só a imagem e o cargo, deixe o nome em branco.

Para um resultado melhor, use uma imagem com traço escuro, de preferência com fundo transparente ou branco liso. Fundos com sombra ou papel amarelado podem deixar manchas.

**Segurança:** as imagens ficam apenas na memória do navegador. Não são enviadas a nenhum servidor e são descartadas ao recarregar a página. Não adicione arquivos de assinatura a este repositório, porque ele é público e qualquer pessoa poderia copiá-los.

### Geração em lote

Disponível em todos os modelos. Marque **Gerar em lote** e informe os alunos um por linha ou separados por ponto e vírgula (`;`). Para incluir a matrícula de cada um, use o formato `Nome, matrícula`:

```
Allan Sabá Peralta Castro, 202312345678
Maria Silva, 202398765432
João Souza
```

O PDF terá uma página por aluno, com os demais dados iguais. A pré-visualização mostra o primeiro aluno da lista. Campos que são individuais por natureza, como o RG do aluno na declaração de visita técnica, ficam ocultos no modo lote.

## Recursos

- Documento em A4 paisagem, com moldura formal e tipografia serifada no título.
- Logotipos da UFPA, do ITEC e do CAEFEL já embutidos no arquivo, com opção de substituí-los pela própria interface.
- Exportação em PDF em alta resolução (aproximadamente 300 dpi). O nome do arquivo é gerado a partir do nome do aluno ou, no lote, da quantidade de alunos.
- Impressão direta, exibindo apenas o documento.

## Observações

- A exportação em PDF e as fontes usam bibliotecas carregadas por CDN (html2canvas, jsPDF e Google Fonts), então é necessário estar conectado à internet. Sem conexão, a página funciona com fontes alternativas e o botão Imprimir continua disponível.
- No modo lote, o botão Imprimir envia uma página por aluno para a impressora.
- Para ativar o GitHub Pages: **Settings → Pages → Source: Deploy from a branch → Branch: `main` / `(root)` → Save**.
