# Google Ads da IHOF — plano para chegar ao nível do Meta

Dados de 30/10/2026. Fontes: conta Meta "iHOF - Dr. Filipe Meireles e Dra. Alynne Paranhos"
(últimos 90 dias) e o funil de campanhas do sistema da clínica (leads de 01/08 a 30/10/2026).

## 1. A régua: o que o Meta entrega hoje

| Métrica (90 dias) | Meta |
|---|---|
| Investimento | R$ 10.179,53 |
| Conversas no WhatsApp/Direct | 1.795 |
| Custo por conversa | ~R$ 5,67 |
| Atendimentos vindos de campanha (sistema da clínica) | 61 |
| Receita desses atendimentos | R$ 88.182,00 |
| Custo por atendimento | ~R$ 167 |
| Retorno (receita ÷ investimento) | ~8,7x |

Por campanha (as que mais pesam):

| Campanha | Investimento Meta | Atendimentos | Receita |
|---|---|---|---|
| Cervicoplastia - All | R$ 4.911,90 | 28 | R$ 43.490,00 |
| Toxina e Preenchimento (Harmonização de Entrada)* | R$ 2.936,22 | 21 | R$ 26.850,00 |
| Protocolos Regenerativos | R$ 304,08 | 7 | R$ 8.420,00 |
| Implantes / Reabilitação Oral | R$ 661,47 | 0 | — |
| Ultrassom Microfocado | R$ 303,79 | 0 | — |

\* A ligação entre a campanha do Meta "Harmonizacao de Entrada" e a campanha "Toxina e
Preenchimento" do sistema é uma suposição pelo nome — confirmar.

**Meta para o Google: custo por atendimento ≤ R$ 170 e retorno ≥ 8x.** Custo por clique e
custo por conversa vão ser bem maiores no Google — isso é normal. O que compensa é a intenção:
quem pesquisa "lipo de papada rio de janeiro" já decidiu que quer o procedimento. Por isso a
comparação tem que ser feita **no atendimento e na receita**, nunca no custo por lead.

O ponto fraco do Meta é a conversão de conversa em atendimento: só ~4% (Cervicoplastia: 1.297
leads → 28 atendimentos). No Google o esperado é 10–20%. É aí que o Google pode empatar ou ganhar.

## 2. Por que provavelmente "não funcionou" antes (checar na conta)

Os erros que mais matam Google Ads de clínica:

1. **Rede de Display e Parceiros de pesquisa ligados** na campanha de Pesquisa → gasto em
   cliques ruins. Desligar os dois.
2. **Performance Max ou "campanha inteligente"** sem conversões confiáveis → o Google otimiza
   para cliques baratos e lixo. Não usar no início.
3. **Sem rastreamento de conversão** (ou contando "clique no WhatsApp" de quem só abriu e
   fechou) → o algoritmo aprende errado.
4. **Correspondência ampla sem negativas** → aparece para "curso de harmonização",
   "harmonização deu errado", "emprego".
5. **Localização em "Presença ou interesse"** → anúncio para quem está fora do Rio.
6. **Orçamento pulverizado** em muitos procedimentos com R$ 20/dia cada.
7. **Texto do anúncio com nome de medicamento** (botox, toxina botulínica, Mounjaro) →
   anúncio reprovado ou limitado pela política de medicamentos com receita.

## 3. Estrutura recomendada (começo)

Só **Pesquisa**, 4 campanhas, seguindo o que já dá dinheiro no Meta:

| Campanha | Por quê | Orçamento/dia inicial |
|---|---|---|
| Search - Lipo de Papada | Maior receita no Meta (R$ 43.490) e busca de alta intenção | R$ 60 |
| Search - Harmonização Facial | Segunda maior receita; termo muito pesquisado | R$ 40 |
| Search - Preenchimento Labial | 3 de 3 agendamentos viraram atendimento | R$ 20 |
| Search - Marca IHOF | Barato, protege o nome contra concorrente | R$ 10 |

Total ≈ **R$ 130/dia ≈ R$ 3.900/mês** — perto de 1/3 do que vai para o Meta. Teste de
60 dias, sem mexer no Meta.

Configurações de cada campanha:

- Rede: só Pesquisa Google (desmarcar Parceiros e Display).
- Local: Rio de Janeiro (Zona Sul, Barra, Recreio, Jacarepaguá, Niterói) —
  **"Presença: pessoas que estão ou costumam estar no local"**.
- Idioma: português. Idade: excluir 18–24 no Lipo de Papada se o público real for mais velho.
- Lances: começar em **Maximizar cliques com CPC máximo de R$ 6** nas 2–3 primeiras semanas;
  ao passar de ~30 conversões/mês na conta, trocar para **Maximizar conversões** e depois
  **CPA desejado** (~R$ 40–60 por conversa qualificada).
- Horário: todos os dias, mas reduzir lance de madrugada (00h–06h) em 50%.
- Recursos: WhatsApp/ligação, local (vincular o Perfil da Empresa das duas unidades),
  sitelinks por procedimento, frases de destaque ("Anestesia local", "Ipanema e Barra").

Arquivos prontos neste diretório:

- `palavras-chave.csv` — palavras por grupo, em frase/exata (nada de ampla no começo).
- `negativas.txt` — lista de negativas para a conta toda.
- `anuncios.csv` — anúncios responsivos (8 títulos ≤ 30 caracteres e 4 descrições ≤ 90),
  sem nome de medicamento. Trocar `SEU-SITE` pela URL real.

Os três arquivos podem ser importados pelo **Google Ads Editor** (Conta → Importar → Colar texto).

## 4. Rastreamento — sem isso não dá para comparar com o Meta

1. **Página de destino por procedimento** (não mandar direto para o WhatsApp): página rápida,
   foto do doutor, 3 provas sociais, botão de WhatsApp fixo. Google pune página fraca com CPC alto.
2. **Conversão principal:** clique no botão de WhatsApp da página (via Google Tag Manager),
   com a mensagem pré-preenchida contendo um código, ex.: `Olá! Vim pelo Google (LP-PAPADA)`.
3. **Cadastrar no sistema da clínica** campanhas com origem "Google" (ex.: "Lipo de Papada —
   Google"), para o funil leads → agendou → atendimento → receita sair separado do Meta. O código
   na mensagem do WhatsApp é o que permite separar.
4. **Conversão de ligação** pelo recurso de ligação (chamadas com mais de 60 s).
5. Depois de 30 dias: **importar conversões offline** (atendimento realizado + valor), para o
   Google otimizar para quem paga, não para quem só manda "oi". É isso que faz o Google passar
   o Meta.

## 5. Cronograma

| Quando | O quê |
|---|---|
| Semana 0 | Conectar Google Ads ao Windsor.ai; auditar conta; criar páginas e conversões; cadastrar campanhas "Google" no sistema |
| Semanas 1–2 | Subir as 4 campanhas; revisar **termos de pesquisa a cada 2–3 dias** e negativar |
| Semanas 3–4 | Pausar palavras com gasto > R$ 150 e zero conversa; passar para Maximizar conversões |
| Dia 30 | 1ª comparação Meta × Google por atendimento e receita |
| Dias 31–60 | CPA desejado; importar conversões offline; testar Protocolos Regenerativos e Implantes |
| Dia 60 | Decisão (abaixo) |

## 6. Regra de decisão no dia 60

- **Custo por atendimento Google ≤ Meta (≈ R$ 170):** aumentar o orçamento do Google 20% a
  cada 2 semanas enquanto o custo se mantiver.
- **Até 1,5x o do Meta:** manter, focar só nas campanhas que fecharam atendimento.
- **Acima de 1,5x:** reduzir para Marca + Lipo de Papada e rever página e palavras.

## 7. Cuidados de publicidade em saúde

- Não citar nome de medicamento (botox, toxina botulínica, Mounjaro) em anúncio nem página do
  Google.
- Não prometer resultado ("garantido", "rejuvenesça 10 anos"), não anunciar preço/promoção
  nem desconto no anúncio, conforme as regras de publicidade do conselho profissional.
- Antes e depois: só dentro do que o conselho permite, e nunca no texto do anúncio.
