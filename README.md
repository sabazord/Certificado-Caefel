# Gerador de Certificados — CAEFEL

Gerador de certificados do **Centro Acadêmico de Engenharia Ferroviária e Logística (CAEFEL)**, da Faculdade de Engenharia Ferroviária e Logística — Instituto de Tecnologia (ITEC) — Universidade Federal do Pará (UFPA).

Aplicação em arquivo único (HTML, CSS e JavaScript). Os dados são preenchidos em um formulário e o certificado é atualizado em tempo real ao lado, pronto para exportar em PDF ou imprimir.

## Como usar

**Online (GitHub Pages):** acesse o link do Pages deste repositório, se estiver ativado.

**Local:** baixe o arquivo `index.html` e abra com duplo clique em qualquer navegador (Chrome, Edge ou Firefox). Não é preciso instalar nada.

1. Preencha o nome do aluno.
2. Escolha o tipo de certificado:
   - **Atividade/Evento:** informe o nome da atividade ou evento.
   - **Membro do Centro Acadêmico:** selecione o cargo exercido na gestão.
3. Informe a carga horária, a categoria (Horas de Extensão ou Horas Complementares) e a data de emissão.
4. Preencha os nomes das três assinaturas: Diretor(a) da Faculdade, Vice-diretor(a) da Faculdade e Presidente do CAEFEL.
5. Clique em **Baixar PDF** ou **Imprimir**.

## Recursos

- Certificado em A4 paisagem, com moldura formal e tipografia serifada no título.
- Texto do corpo montado automaticamente conforme o tipo de certificado.
- Logotipos da UFPA, do ITEC e do CAEFEL já embutidos no arquivo, com opção de substituí-los pela própria interface.
- Exportação em PDF em alta resolução (aproximadamente 300 dpi), com o nome do arquivo gerado a partir do nome do aluno.
- Impressão direta, exibindo apenas o certificado.

## Observações

- A exportação em PDF e as fontes usam bibliotecas carregadas por CDN (html2canvas, jsPDF e Google Fonts), então é necessário estar conectado à internet. Sem conexão, a página funciona com fontes alternativas e o botão Imprimir continua disponível.
- Para ativar o GitHub Pages: **Settings → Pages → Source: Deploy from a branch → Branch: `main` / `(root)` → Save**.
