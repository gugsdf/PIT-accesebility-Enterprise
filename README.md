# ♿ Acessibilidade Digital — Tecnologia para Todos

> Projeto de pesquisa e auditoria de acessibilidade digital em empresas reais, desenvolvido pelo **Grupo J&F** do Instituto J&F.
>
> **Integrantes:** Felipe Kogake, Gustavo Souza, Igor Quinto, Luiza De Vicente
> **Data das Análises:** Abril de 2026

---

## 📌 Sobre esta pesquisa

Esta pesquisa avalia como empresas brasileiras e globais de diferentes setores implementam (ou ignoram) a acessibilidade digital em suas plataformas — investigando se produtos digitais reais são verdadeiramente inclusivos para os mais de 18 milhões de brasileiros com deficiência, ou se a conformidade técnica ainda é tratada como acessório e não como fundamento do desenvolvimento.

---

## 🔍 O que descobrimos (Principais Achados)

- **Conformidade técnica não garante inclusão real:** o site da JBS atingiu 100/100 no Lighthouse e 0 erros no Axe Tools, mas ainda carece de atalhos de teclado eficientes e audiodescrição em imagens — mostrando que notas máximas coexistem com barreiras práticas de uso. *(Fonte: Relatório de Auditoria JBS, Grupo J&F, 2026)*

- **Fintechs lideram em acessibilidade de produto, mas ficam atrás na conformidade técnica:** o Nubank possui atendimento em Libras 24/7, cartão em Braille (NuBraille) e contratos em áudio — recursos inexistentes na maioria das empresas — mas obteve apenas 80/100 no Lighthouse, com falhas em contraste e links sem descrição. *(Fonte: Relatório de Auditoria Nubank, Grupo J&F, 2026)*

- **A Apple representa o padrão ouro em acessibilidade sistêmica:** ao integrar recursos como Eye Tracking, Personal Voice e VoiceOver diretamente no sistema operacional, a empresa elimina a dependência de soluções de terceiros — abordagem que nenhuma empresa brasileira analisada replicou plenamente. *(Fonte: Relatório de Auditoria Apple, Grupo J&F, 2026)*

- **Ignorar acessibilidade tem custo financeiro e reputacional comprovado:** a Enel foi multada em R$ 1.241.838,00 pelo MPCE por não oferecer recursos básicos de acessibilidade em seu site; nos EUA, a Domino's perdeu na Suprema Corte o direito de manter seu app inacessível. *(Fonte: MPCE/DECON, 2024; Robles v. Domino's Pizza, 9th Circuit, 2019)*

- **Problemas recorrentes independem do porte da empresa:** botões sem nomes acessíveis, `tabindex` fora de ordem e alvos de toque pequenos apareceram nos sites da Apple (89/100) e do PicPay (77/100) — indicando que esses erros básicos são sistêmicos no mercado, não exceção. *(Fonte: Relatórios de Auditoria Apple e PicPay, Grupo J&F, 2026)*

---

## 🛠 Ferramentas / Casos / Legislação

### Ferramentas de Auditoria

#### Google Lighthouse
Ferramenta automatizada do Google que avalia páginas web em quatro categorias: Desempenho, Acessibilidade, Boas Práticas e SEO. As pontuações variam de 0 a 100:

| Faixa | Classificação |
|-------|--------------|
| 0–49 | ❌ Ruim |
| 50–89 | ⚠️ Precisa de atenção |
| 90–100 | ✅ Bom |

> ⚠️ O Lighthouse é automatizado e limitado — identifica apenas parte dos problemas. Testes manuais com usuários reais são indispensáveis para garantir acessibilidade plena.

#### Axe DevTools
Desenvolvido pela Deque Systems, é considerado a ferramenta de auditoria mais rigorosa do mercado. Baseia-se estritamente nas diretrizes **WCAG** e foca em eliminar falsos positivos — só aponta erros comprovadamente críticos. Zero issues no Axe equivale ao padrão ouro de conformidade técnica.

---

### 🏢 Empresas Analisadas

#### 🍎 Apple — Pontuação Lighthouse: 89/100

A Apple se destaca por integrar recursos de acessibilidade diretamente no sistema operacional, combinando hardware e software de forma nativa.

**Principais recursos:**
- **VoiceOver** — leitor de tela baseado em gestos
- **Lupa / Modo de Detecção** — detecta objetos, portas e pessoas com a câmera
- **Eye Tracking** — navegação pelo iPhone usando apenas o movimento dos olhos (iOS 18)
- **Personal Voice** — voz sintética personalizada para pessoas com risco de perda de fala
- **Live Speech** — converte texto digitado em fala durante chamadas
- **AssistiveTouch para Apple Watch** — controle por movimentos de mão
- **RTT / Texto em Tempo Real** — chamadas de texto para usuários com deficiência auditiva

**Pontos de atenção:** botões sem nomes acessíveis, uso de `tabindex` maior que zero e alvos de toque pequenos em mobile.

---

#### 💜 Nubank — Pontuação Lighthouse: 80/100

O Nubank trata inclusão como estratégia institucional, não apenas como conformidade técnica.

**Principais recursos:**
- **Atendimento em Libras 24/7** integrado ao aplicativo
- **NuBraille** — cartão com informações em Braille, com kit de instruções em áudio e vídeo
- **NuAcessível e NuLibras** — playlists com conteúdo financeiro acessível em Libras
- **Contratos acessíveis** em formato visual + áudio
- **Modo Escuro** para conforto visual e usuários com fotofobia
- **Navegação por teclado e ARIA** no site institucional

**Pontos de atenção:** ausência de auditoria técnica pública completa; falta de evidências sobre navegação por teclado no app mobile.

---

#### 🟢 PicPay — Pontuação Lighthouse: 77/100

O PicPay apresenta uma base razoável de acessibilidade web, mas ainda sem recursos avançados integrados ao produto.

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

#### 🔵 JBS — Pontuação Lighthouse: 100/100 | Axe Tools: 0 issues

O site da JBS é um benchmark no setor industrial brasileiro, com notas máximas nas ferramentas de auditoria automatizada.

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

### 📊 Mapa Comparativo (Benchmark)

| Empresa | Maturidade e Estratégia | Cobertura de Deficiências | Recursos de Acessibilidade | Experiência do Usuário (UX) | Conformidade Técnica |
|---------|:-:|:-:|:-:|:-:|:-:|
| **JBS** | ✅ Alto | ✅ Alto | ➖ Regular | ➖ Regular | ✅ Alto |
| **PicPay** | ✅ Alto | ✅ Alto | ➖ Regular | ✅ Alto | ➖ Regular |
| **Nubank** | ✅ Alto | ➖ Regular | ✅ Alto | ✅ Alto | ➖ Regular |
| **Apple** | ✅ Alto | ✅ Alto | ✅ Alto | ✅ Alto | ➖ Regular |

---

### ⚖️ Legislação e Casos de Sanção

#### Domino's Pizza (EUA)
Em 2016, Guillermo Robles, um usuário cego, processou a rede por não conseguir fazer pedidos pelo site e app utilizando leitor de tela. Tribunais decidiram que plataformas digitais são extensões das lojas físicas e devem ser acessíveis. A Suprema Corte dos EUA recusou o recurso da empresa em 2019, consolidando o precedente.

**Consequências:** danos à reputação e altos custos advocatícios.

#### Enel (Brasil — Ceará)
O DECON (Ministério Público do Ceará) constatou em fiscalização online que o site da Enel não possuía recursos básicos de acessibilidade. A empresa argumentou ter um projeto global em desenvolvimento, mas a justificativa foi rejeitada por não cumprir as normativas vigentes.

**Consequências:** multa de **R$ 1.241.838,00** por exclusão digital de consumidores com deficiência. *(Notificação: 17 de dezembro de 2024)*

#### Base Legal Brasileira
A **Lei Brasileira de Inclusão (Lei 13.146/2015)** — também chamada de Estatuto da Pessoa com Deficiência — estabelece que o acesso à informação e comunicação, inclusive por meio da internet, é direito fundamental. O descumprimento sujeita empresas a sanções administrativas e civis.

> ⚠️ Esses casos demonstram que a acessibilidade digital deixou de ser uma recomendação técnica e passou a ser uma **exigência legal com impacto financeiro e reputacional imediato**.

---

## 👨‍💻 Como isso afeta o nosso trabalho como desenvolvedores

Adotar uma política de acessibilidade exige uma mudança de mentalidade: o desenvolvedor deixa de pensar apenas em funcionalidade e visual e passa a construir para a diversidade humana. Na prática, isso significa incorporar ao fluxo de trabalho pelo menos três práticas concretas:

---

**1. Usar HTML semântico e atributos ARIA corretamente**

Leitores de tela dependem da estrutura do HTML para interpretar a página. Usar `<button>` em vez de `<div>` para ações, associar `<label>` a `<input>`, e descrever elementos interativos com `aria-label` são requisitos básicos — não opcionais.

```html
<!-- ❌ Inacessível: leitor de tela lê "botão sem nome" -->
<div onclick="enviar()">
  <img src="seta.svg" />
</div>

<!-- ✅ Acessível: leitor de tela lê "Enviar formulário" -->
<button onclick="enviar()" aria-label="Enviar formulário">
  <img src="seta.svg" alt="" aria-hidden="true" />
</button>
```

---

**2. Garantir navegação funcional por teclado**

Todos os fluxos críticos (login, formulários, checkout) devem funcionar sem mouse. Isso inclui nunca usar `tabindex` maior que zero — que quebra a ordem lógica de navegação, problema identificado tanto no site da Apple quanto no PicPay — e sempre garantir que o indicador de foco seja visível.

```css
/* ❌ Inacessível: esconde o indicador de foco */
:focus {
  outline: none;
}

/* ✅ Acessível: foco visível e com bom contraste */
:focus-visible {
  outline: 3px solid #005fcc;
  outline-offset: 2px;
  border-radius: 4px;
}
```

---

**3. Integrar testes de acessibilidade ao pipeline de desenvolvimento**

Ferramentas como Lighthouse e Axe DevTools podem ser executadas automaticamente a cada Pull Request, evitando regressões. Mas testes automatizados sozinhos não bastam — simulações com leitores de tela (NVDA, VoiceOver, TalkBack) e sessões com usuários com deficiência revelam barreiras que nenhuma ferramenta captura.

```bash
# Rodar Lighthouse via CLI e exibir pontuação de acessibilidade
npx lighthouse https://meusite.com \
  --only-categories=accessibility \
  --output=json \
  --output-path=./lighthouse-report.json

cat lighthouse-report.json | python3 -c \
  "import json,sys; r=json.load(sys.stdin); \
   print('Acessibilidade:', r['categories']['accessibility']['score']*100)"
```

> 💡 **Regra prática:** se um usuário cego, um usuário usando apenas teclado e um usuário com baixa visão conseguirem completar os fluxos principais do produto sem assistência, a base de acessibilidade está sólida.

---

## 📚 Referências

1. **Brasil. Presidência da República.** Lei Brasileira de Inclusão da Pessoa com Deficiência (Lei nº 13.146/2015). 2015. http://www.planalto.gov.br/ccivil_03/_ato2015-2018/2015/lei/l13146.htm

2. **W3C — World Wide Web Consortium.** Web Content Accessibility Guidelines (WCAG) 2.1. 2018. https://www.w3.org/TR/WCAG21/

3. **Google Developers.** Lighthouse — Visão Geral. 2024. https://developer.chrome.com/docs/lighthouse/overview/

4. **Deque Systems.** Axe DevTools — Accessibility Testing. 2024. https://www.deque.com/axe/devtools/

5. **Ministério Público do Estado do Ceará (MPCE/DECON).** DECON multa Enel em R$ 1,2 milhão por falta de acessibilidade no site da concessionária. 2024. https://mpce.mp.br/decon-multa-enel-em-r-12-milhao-por-falta-de-acessibilidade-no-site-da-concessionaria/

6. **United States Court of Appeals, Ninth Circuit.** Robles v. Domino's Pizza LLC (No. 17-55504). 2019. https://law.justia.com/cases/federal/appellate-courts/ca9/17-55504/17-55504-2019-01-15.html

7. **Grupo J&F — Instituto J&F.** Relatórios de Auditoria de Acessibilidade Digital: Apple, Nubank, PicPay e JBS. Abril de 2026. *(Documentos internos do projeto)*

---

*Instituto J&F — Acessibilidade Digital: Tecnologia para Todos | Abril de 2026*
