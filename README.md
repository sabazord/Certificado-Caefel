# Gerador de Certificados — CAEFEL

Gerador de certificados e declarações do **Centro Acadêmico de Engenharia Ferroviária e Logística (CAEFEL)**, da Faculdade de Engenharia Ferroviária e Logística — Instituto de Tecnologia (ITEC) — Universidade Federal do Pará (UFPA).

Aplicação em arquivo único (HTML, CSS e JavaScript). Os dados são preenchidos em um formulário e o documento é atualizado em tempo real ao lado, pronto para exportar em PDF ou imprimir.

## Modelos de documento

| Modelo | Título | Campos específicos |
|---|---|---|
| Participação em evento | CERTIFICADO | Nome da atividade/evento, carga horária, categoria de horas. Aceita geração em lote. |
| Declaração de visita técnica | DECLARAÇÃO | RG do aluno, professor(a) e RG, disciplina, local, cidade/UF, carga horária (todos opcionais) |
| Membro do CAEFEL | CERTIFICADO | Cargo na gestão, carga horária, categoria de horas |
| Monitoria | CERTIFICADO | Disciplina, professor(a) orientador(a), período, carga horária |
| Minicurso | CERTIFICADO | Título, ministrante, data/período, carga horária, promotor |

O texto do corpo é montado automaticamente conforme o modelo escolhido e os campos preenchidos. Campos opcionais desmarcados são omitidos do texto.

## Como usar

**Online (GitHub Pages):** acesse `https://sabazord.github.io/Certificado-Caefel/`, se o Pages estiver ativado.

**Local:** baixe o arquivo `index.html` e abra com duplo clique em qualquer navegador (Chrome, Edge ou Firefox). Não é preciso instalar nada.

1. Escolha o modelo de documento.
2. Preencha o nome do aluno e, se quiser, a matrícula.
3. Preencha os campos específicos do modelo e a data de emissão.
4. Preencha os nomes das assinaturas: Diretor(a) da Faculdade, Vice-diretor(a) da Faculdade e Presidente do CAEFEL. Qualquer uma pode ser removida do documento pelo botão ✕ e restaurada depois.
5. Clique em **Baixar PDF** ou **Imprimir**.

### Geração em lote

No modelo de participação em evento, marque **Gerar em lote** e informe os nomes separados por ponto e vírgula (`;`). O PDF terá uma página por aluno, com os demais dados iguais.

## Recursos

- Documento em A4 paisagem, com moldura formal e tipografia serifada no título.
- Logotipos da UFPA, do ITEC e do CAEFEL já embutidos no arquivo, com opção de substituí-los pela própria interface.
- Exportação em PDF em alta resolução (aproximadamente 300 dpi). O nome do arquivo é gerado a partir do nome do aluno ou, no lote, da quantidade de alunos.
- Impressão direta, exibindo apenas o documento.

## Observações

- A exportação em PDF e as fontes usam bibliotecas carregadas por CDN (html2canvas, jsPDF e Google Fonts), então é necessário estar conectado à internet. Sem conexão, a página funciona com fontes alternativas e o botão Imprimir continua disponível.
- O botão Imprimir gera apenas o documento exibido na pré-visualização. No lote, use **Baixar PDF** para obter todos os alunos.
- Para ativar o GitHub Pages: **Settings → Pages → Source: Deploy from a branch → Branch: `main` / `(root)` → Save**.
