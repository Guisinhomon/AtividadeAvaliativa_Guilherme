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
  
# 4. Requisitos Não Funcionais (mínimo 4)

RNF01 — O sistema deve ser rápido e responder às ações do usuário sem travar  

RNF02 — O sistema deve ser seguro, garantindo que só usuários autorizados acessem certas funções  

RNF03 — O sistema deve funcionar 24 horas, já que a farmácia pode precisar de consultas a qualquer momento  

RNF04 — O sistema deve ser fácil de usar, com interface simples pra atendentes, gerentes e farmacêuticos

---

# 5. Casos de Uso (mínimo 10)

Meus atores
 Atendente  
 Cliente  
 Gerente  
 Finaanceiro  

Casos de Uso

UC01 — Cadastrar/Identificar Cliente  
UC02 — Consultar Produto  
UC03 — Verificar Estoque  
UC04 — Registrar Venda  
UC05 — Emitir Comprovante de Venda  
UC06 — Registrar Venda a Prazo  
UC07 — Atualizar Estoque  
UC08 — Consultar Histórico de Vendas do Cliente  
UC09 — Gerenciar Produtos (cadastrar/editar)  
UC10 — Gerar Contas a Receber  

### Relações Include e Extend

 Include (sempre acontece dentro do processo):
 Registrar Venda <<include>> Verificar Estoque  
 Registrar Venda <<include>> Cadastrar/Identificar Cliente  
 Registrar Venda a Prazo <<include>> Registrar Venda  

 Extend (acontece só em algumas situações):  
 Emitir Comprovante de Venda <<extend>> Registro de Venda  
 Registrar Venda a Prazo <<extend>> Gerar Contas a Receber  
 Consultar Histórico de Vendas do Cliente <<extend>> Cadastrar/Identificar Cliente  

 Foto do Diagrama:

 
 <img width="508" height="1026" alt="image" src="https://github.com/user-attachments/assets/3bd11278-8846-430d-b235-96dacf4779c3" />


---
