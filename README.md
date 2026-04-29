# ♿ Acessibilidade Digital — Tecnologia para Todos

> Projeto de pesquisa e auditoria de acessibilidade digital em empresas reais, desenvolvido pelo **Grupo J&F** do Instituto J&F.
>
> **Integrantes:** Felipe Kogake, Gustavo Souza, Igor Quinto, Luiza De Vicente
> **Data das Análises:** Abril de 2026

---

## 📌 Sobre o Projeto

Este projeto investiga como empresas reais implementam (ou ignoram) a acessibilidade digital em suas plataformas. A metodologia combina validações técnicas automatizadas com análise de experiência do usuário (UX), avaliando quatro pilares fundamentais:

- 👁 **Visual** — compatibilidade com leitores de tela, contraste, textos alternativos
- 👂 **Auditiva** — legendas, Libras, alternativas ao áudio
- 🖱 **Motora** — navegação por teclado, alvos de toque, foco visível
- 🧠 **Cognitiva** — linguagem simples, consistência visual, clareza de feedback

---

## 🛠 Ferramentas Utilizadas

### Google Lighthouse
Ferramenta automatizada do Google que avalia páginas web em quatro categorias: Desempenho, Acessibilidade, Boas Práticas e SEO. As pontuações variam de 0 a 100:

| Faixa | Classificação |
|-------|--------------|
| 0–49 | ❌ Ruim |
| 50–89 | ⚠️ Precisa de atenção |
| 90–100 | ✅ Bom |

### Axe DevTools
Desenvolvido pela Deque Systems, é considerado a ferramenta de auditoria de acessibilidade mais rigorosa do mercado. Baseia-se estritamente nas diretrizes **WCAG** (Web Content Accessibility Guidelines) e foca em eliminar falsos positivos — só aponta erros comprovadamente críticos.

---

## 🏢 Empresas Analisadas

### 🍎 Apple
**Pontuação Lighthouse (acessibilidade):** 89/100

A Apple se destaca por integrar recursos de acessibilidade diretamente em seus sistemas operacionais, oferecendo soluções nativas que combinam hardware e software.

**Principais recursos:**
- **VoiceOver** — leitor de tela baseado em gestos
- **Lupa / Modo de Detecção** — detecta objetos, portas e pessoas com a câmera
- **Eye Tracking** — navegação pelo iPhone usando apenas o movimento dos olhos (iOS 18)
- **Personal Voice** — cria uma voz sintética personalizada para pessoas com risco de perda de fala
- **Live Speech** — converte texto digitado em fala durante chamadas
- **AssistiveTouch para Apple Watch** — controle por movimentos de mão
- **RTT / Texto em Tempo Real** — chamadas de texto para usuários com deficiência auditiva

**Pontos de atenção:** botões sem nomes acessíveis, uso de `tabindex` maior que zero e alvos de toque pequenos em mobile.

---

### 💜 Nubank
**Pontuação Lighthouse (acessibilidade):** 80/100

O Nubank apresenta alto nível de maturidade em acessibilidade, tratando a inclusão como parte estratégica do negócio e não apenas como conformidade técnica.

**Principais recursos:**
- **Atendimento em Libras 24/7** integrado ao aplicativo
- **NuBraille** — cartão com informações em Braille (nome e últimos dígitos), com kit de instruções em áudio e vídeo
- **NuAcessível e NuLibras** — playlists com conteúdo financeiro acessível
- **Contratos acessíveis** em formato visual + áudio
- **Modo Escuro** para conforto visual e usuários com fotofobia
- **Navegação por teclado e ARIA** no site institucional

**Pontos de atenção:** ausência de auditoria técnica pública completa; falta de evidências detalhadas sobre navegação por teclado no app mobile.

---

### 🟢 PicPay
**Pontuação Lighthouse (acessibilidade):** 77/100

O PicPay apresenta uma base razoável de acessibilidade, com boas práticas de desenvolvimento web, mas ainda sem recursos tão avançados quanto grandes empresas de tecnologia.

**Pontos positivos:**
- Uso correto de atributos **ARIA**
- **Legendas** nos vídeos institucionais
- Contraste de cores adequado na maioria dos textos
- Layout responsivo com suporte a zoom

**Pontos de atenção:**
- Botões sem nomes acessíveis (dificulta leitores de tela)
- `tabindex` maior que zero comprometendo a ordem de navegação por teclado
- Alvos de toque pequenos ou próximos demais em mobile
- Formulários de cadastro/login sem associação correta de rótulos
- Mensagens de erro pouco descritivas

---

### 🔵 JBS
**Pontuação Lighthouse (acessibilidade):** 100/100 | **Axe Tools:** 0 issues

O site da JBS é um benchmark no setor industrial brasileiro, sendo classificado como referência técnica com notas máximas nas ferramentas de auditoria.

**Principais recursos:**
- **Widget VLibras** — tradução de todo o conteúdo para Libras via avatares 3D
- **Alto contraste de cores** — paleta corporativa com índices de contraste adequados
- **Marcação semântica** — código etiquetado corretamente para leitores de tela
- **Navegação via teclado** funcional
- **Layout limpo** com bastante espaço em branco, evitando sobrecarga cognitiva
- Investimento em atendimento ao cliente em Libras (marcas Friboi e Seara)

**Pontos de atenção:**
- Ausência de atalhos "Ir direto para o conteúdo" em páginas longas
- Alt Text incompleto em algumas imagens institucionais
- Linguagem técnica em seções de RI e ESG (sem resumos em linguagem simples)
- Ausência de audiodescrição (#ParaTodosVerem) em galerias e blog

---

## 📊 Benchmark Comparativo

| Empresa | Maturidade e Estratégia | Cobertura de Deficiências | Recursos de Acessibilidade | Experiência do Usuário (UX) | Conformidade Técnica |
|---------|:-:|:-:|:-:|:-:|:-:|
| **JBS** | ✅ Alto | ✅ Alto | ➖ Regular | ➖ Regular | ✅ Alto |
| **PicPay** | ✅ Alto | ✅ Alto | ➖ Regular | ✅ Alto | ➖ Regular |
| **Nubank** | ✅ Alto | ➖ Regular | ✅ Alto | ✅ Alto | ➖ Regular |
| **Apple** | ✅ Alto | ✅ Alto | ✅ Alto | ✅ Alto | ➖ Regular |

---

## ⚖️ Empresas Multadas por Falta de Acessibilidade

### Domino's Pizza (EUA)
Em 2016, Guillermo Robles, um usuário cego, processou a rede por não conseguir fazer pedidos pelo site e aplicativo utilizando um leitor de tela. Tribunais de recursos decidiram que sites e aplicativos são extensões das lojas físicas e devem ser acessíveis. A Suprema Corte dos EUA recusou o recurso da empresa em 2019.

**Consequências:** danos à reputação e altos custos advocatícios.

### Enel (Brasil — Ceará)
O Ministério Público do Ceará (DECON) constatou que o site da Enel não possuía recursos básicos de acessibilidade. A empresa argumentou que estava desenvolvendo um projeto global, mas a justificativa foi rejeitada por não cumprir as normativas vigentes.

**Consequências:** multa de **R$ 1.241.838,00** por exclusão digital de consumidores com deficiência.

> ⚠️ Esses casos demonstram que a acessibilidade digital deixou de ser uma recomendação e passou a ser uma **exigência legal com impacto financeiro e reputacional imediato**.

---

## 👨‍💻 Impacto no Trabalho do Desenvolvedor

Quando uma empresa adota uma política de acessibilidade, o trabalho do desenvolvedor passa por uma mudança significativa de mentalidade. Ele deixa de focar apenas em funcionalidade e aparência e passa a considerar:

- **Usabilidade para todos os públicos** — incluindo pessoas com deficiências visual, auditiva, motora ou cognitiva
- **HTML semântico** — uso correto de tags e atributos para que leitores de tela interpretem a estrutura corretamente
- **Leitores de tela** — testes com ferramentas como NVDA, JAWS e VoiceOver
- **Navegação por teclado** — garantir que todos os fluxos funcionem sem mouse
- **Código estruturado e padronizado** — conformidade com WCAG 2.1 nível AA como meta mínima

---

## 📚 Referências

- [Lei Brasileira de Inclusão (Lei 13.146/2015)](http://www.planalto.gov.br/ccivil_03/_ato2015-2018/2015/lei/l13146.htm)
- [WCAG 2.1 — W3C](https://www.w3.org/TR/WCAG21/)
- [Google Lighthouse](https://developer.chrome.com/docs/lighthouse/overview/)
- [Axe DevTools — Deque Systems](https://www.deque.com/axe/devtools/)
- [MPCE — Multa Enel por falta de acessibilidade](https://mpce.mp.br/decon-multa-enel-em-r-12-milhao-por-falta-de-acessibilidade-no-site-da-concessionaria/)
- [Site oficial JBS](https://www.jbs.com.br/)

---

*Instituto J&F — Acessibilidade Digital: Tecnologia para Todos | Abril de 2026*
