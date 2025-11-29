# Grupo Primavera — Site Institucional e Prototipação
veja mais aqui:https://gabrielacpires16-dev.github.io/slide/#slide-1

Demo / Base do projeto: arquivo fornecido (grupo-primavera.html)

Este repositório contém o protótipo do site institucional do Grupo Primavera — uma Organização da Sociedade Civil que atende crianças, adolescentes e jovens do entorno do Jardim São Marcos (Campinas, SP). O site reúne informações institucionais, programas, formas de ajudar (doações, voluntariado), conteúdos educativos e jogos lúdicos para divulgação e engajamento.

O objetivo deste README é documentar o protótipo, o fluxo de uso, os artefatos de design (diagrama de casos de uso e protótipos de tela) e orientar próximos passos para desenvolvimento e entrega.

---

## 📘 Sobre o Projeto

O site/protótipo apresenta a identidade visual do Grupo Primavera, com destaque para:
- Hero com CTA para Doação e Conhecer o Trabalho.
- Seções: Sobre, Impacto, Programas, Joguinhos (educativos), Como Ajudar, Contato.
- Blocos de estatísticas (anos de atividade, vidas transformadas, atendimentos).
- Funkcionalidades interativas: jogos (memory, quiz, coletor de corações) e modal de jogo.
- Design responsivo e animações leves (float, pulse, beats).

A página é construída com HTML/CSS/JS, utilizando Tailwind via CDN e scripts inline para interatividade.

---

## 🚩 Principais Funcionalidades (visão do site)

- Hero com CTAs: "Faça sua Doação" e "Conheça Nosso Trabalho".
- Seção "Sobre": missão, visão, público atendido.
- "Nosso Impacto": estatísticas destacadas (anos, vidas, atendidos, aprovação).
- "Nossos Programas": Educação Complementar, Cultura e Arte, Formação Profissional.
- "Joguinhos Educativos": mini‑games para engajamento (Memory, Quiz, Heart Collector).
- "Como Você Pode Ajudar": PIX/CNPJ, voluntariado, Nota Fiscal Paulista, Imposto de Renda.
- Contato com endereço, telefone e email; links para redes sociais.
- Pequeno painel / scripts que permitem testes de interação com jogos e animações.

---

## 🧭 Diagrama de Casos de Uso (simplificado)

Abaixo, uma representação ASCII do diagrama de casos de uso principal para o site / futuro sistema digital de apoio à ONG:

```
+-------------------+     +-------------------+
|    Visitante      |     |    Voluntário     |
+-------------------+     +-------------------+
| - Ver conteúdos   |     | - Candidatar-se   |
| - Doar            |     | - Ver vagas       |
+-------------------+     +-------------------+
          |                          |
          v                          v
+-----------------------------------------------+
|           Sistema / Site Grupo Primavera      |
+-----------------------------------------------+
| Use Cases:                                    |
| - Visualizar Home / Programas / Impacto       |
| - Acessar Joguinhos Educativos                 |
| - Doar via PIX (informativo)                   |
| - Cadastrar interesse em voluntariado          |
| - Enviar contato / consultar endereço/telefone |
+-----------------------------------------------+
```

- Atores: Visitante (público), Voluntário (pessoa interessada), Empresa (parceira) — e internamente Gestores que recebem contatos/solicitações.
- Observação: o protótipo atual foca em divulgação e interação; funcionalidades de backend (registro de doações, gestão de voluntários) são propostas para evolução.

---

## 🎨 Protótipos de Tela (descrição)

Os wireframes/elementos visuais foram extraídos do arquivo HTML e estão prontos para serem transformados em protótipos clicáveis (Figma):

- Tela Hero
  - Título grande, subtítulo, CTAs (Doar / Conhecer).
  - Ilustração/ícone com corações.

- Seção Sobre
  - Texto institucional, missão e histórico.

- Programas
  - Cards para Educação Complementar, Cultura e Arte, Formação Profissional.

- Impacto
  - Cartões estatísticos com destaque numérico.

- Joguinhos Educativos
  - Cards com CTA "Jogar Agora" que abrem modais com os jogos (Memory, Quiz, Heart Collector).

- Como Ajudar
  - Cartões para PIX (QR placeholder), voluntariado, Nota Fiscal Paulista e Imposto de Renda.

- Contato
  - Formato com endereço, telefone e email; botões para redes sociais.

Cada protótipo inclui observações UX:
- Chamadas à ação bem visíveis (Doar).
- Fluxos simples: Home → PACTO/Doação/Voluntariado → Confirmação/Contato.
- Acessibilidade básica: contraste e tamanhos adequados (precisa ser refinada para WCAG).

---

## 🛠 Tecnologias e Arquitetura

- HTML5 (estrutura e semântica)
- CSS3 + Tailwind (via CDN) — estilos principais e utilitários
- JavaScript (ES6+) — interações, modais e minigames
- Arquivo principal: `grupo-primavera.html` (protótipo auto‑contido)
- Observação: para persistência e funcionalidades administrativas, é necessária implementação de backend (API + banco de dados). Atualmente o protótipo é front-end e demonstrativo.

---

## ▶️ Executar localmente / Como testar

1. Baixe ou clone o repositório contendo `grupo-primavera.html`.
2. Abra o arquivo `grupo-primavera.html` em um navegador moderno (Chrome / Firefox / Edge).
3. Navegue nas seções: use o menu ou âncoras; clique nos jogos e modais para testar interatividade.
4. Para desenvolvimento local com servidor estático (opcional):
   - Python: `python -m http.server 8000` → abra http://localhost:8000/grupo-primavera.html

---

## ✅ Recomendações para evolução (roadmap curto)

Prioridade alta:
- Implementar formulário seguro para voluntariado (back-end) e salvar candidaturas.
- Implementar mecanismo de doação integrado (ou redirecionar para gateway confiável) e registro de comprovantes.
- Criar painel administrativo para triagem de denúncias/contatos/voluntariado.

Prioridade média:
- Migrar estilos para um design system (tokens + componentes).
- Criar protótipos de alta fidelidade no Figma e rodar testes de usabilidade.
- Implementar acessibilidade (WCAG 2.1 AA).

Prioridade baixa:
- Internacionalização (pt‑BR + en).
- Automação de testes end‑to‑end para fluxos críticos.

---

## 🧪 Plano de Testes (resumo)

Testes manuais prioritários:
- Fluxo de navegação (links e âncoras).
- Abertura e fechamento de modais (jogos).
- Joguinhos: Playability e encerramento (scores e telas finais).
- Formulários de contato/voluntariado (validações, envio — quando implementado back-end).

Ferramentas sugeridas (futuro):
- Playwright / Cypress para E2E
- Lighthouse para performance e acessibilidade

---

## 🤝 Contribuição

Se quiser colaborar:
- Abra uma issue explicando a proposta.
- Faça um fork do repositório e crie um branch (`feat/meu-recurso` ou `fix/bug`).
- Submeta um Pull Request com descrição e passos para testar.

Guidelines:
- Use mensagens de commit claras.
- Inclua imagens ou GIFs quando alterar a interface.

---

## 📄 Licença

Protótipo fornecido para fins educacionais e demonstrativos. Escolha uma licença apropriada para produção (por exemplo MIT) antes de redistribuir.

---

## ✍️ Credits / Autor

Projeto e prototipação: **Grupo Primavera**  
Design / apresentação: **Gabriela Pires**

---
