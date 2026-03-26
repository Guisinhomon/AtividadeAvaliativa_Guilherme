Avaliação — Engenharia de Software
**Sistema Integrado de Gestão de Farmácia

Aluno: *Guilherme Alan Vilela Silva*  
RA: *25001363*  
Data: *25/03/2026*  

---

# 1. Definição do MVP

Pro meu MVP eu resolvi focar na parte de vendas da farmácia, tipo desde identificar ou cadastrar o cliente até terminar a venda e emitir o comprovante.

Dentro do MVP
- Cadastrar e identificar clientes
- Consultar produtos
- Verificar estoque
- Registrar vendas à vista e a prazo
- Atualizar o estoque automaticamente depois da venda
- Gerar contas a receber pras vendas a prazo
- Emitir comprovante de venda

Fora do MVP
- Gerenciar compras e fornecedores
- Fazer relatórios e indicadores
- Controle mais avançado de usuários e permissões
- Transferência de estoque entre unidades

Justificativa
Escolhi focar nisso porque vender é a parte que acontece o tempo todo na farmácia e envolve várias coisas do sistema tipo estoque, clientes e financeiro. Então faz mais sentido começar por aí pra garantir que funcione bem. As outras coisas também são importantes, mas dá pra deixar pra depois sem atrapalhar o básico do sistema.

---

# 2. Regras de Negócio (mínimo 5)

RN01 — O sistema não pode permitir a venda de produtos que não tenham estoque disponível  

RN02 — Toda venda deve atualizar automaticamente o estoque da farmácia  

RN03 — Vendas a prazo devem gerar automaticamente uma conta a receber pro cliente  

RN04 — Clientes precisam estar cadastrados pra conseguir comprar a prazo  

RN05 — Compras feitas pelos fornecedores devem atualizar o estoque e gerar contas a pagar pro financeiro
(Adicione mais se quiser.)

---

# 3. Requisitos Funcionais (mínimo 8)

RF01 — O sistema deve permitir cadastrar e identificar clientes  

RF02 — O sistema deve permitir consultar produtos disponíveis  

RF03 — O sistema deve verificar automaticamente se o produto tem estoque antes da venda  

RF04 — O sistema deve registrar vendas à vista  

RF05 — O sistema deve registrar vendas a prazo e gerar contas a receber  

RF06 — O sistema deve atualizar automaticamente o estoque depois de cada venda  

RF07 — O sistema deve emitir um comprovante de venda pro cliente  

RF08 — O sistema deve permitir consultar o histórico de vendas de cada cliente

---
