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

# 6. Documentação dos Casos de Uso

UC01 — Cadastrar/Identificar Cliente

Atores: Atendente, Cliente
Descrição: Identifica ou cadastra cliente para vincular vendas.
Pré-condições: Cliente precisa ser identificado.
Pós-condições: Cliente registrado no sistema.
Fluxo Principal: Pesquisa cliente → Se não existir, cadastra → Confirma identificação.
Fluxos Alternativos: Cliente não encontrado → cadastra; Dados inválidos → corrige.

**Foto do Diagrama:**


<img width="394" height="440" alt="image" src="https://github.com/user-attachments/assets/6b84924e-4140-430e-8a37-5e7252a5f981" />


UC02 — Consultar Produto

Ator: Atendente
Descrição: Pesquisa produto pelo nome, código ou fabricante.
Pré-condições: Produto cadastrado no sistema.
Pós-condições: Produto localizado.
Fluxo Principal: Digita critério → Sistema mostra produtos → Seleciona produto.
Fluxos Alternativos: Produto não encontrado → mensagem; Dados incorretos → corrige.


**Foto do Diagrama:**


<img width="385" height="374" alt="image" src="https://github.com/user-attachments/assets/b9e6dc85-a467-4832-9d24-73123c30e84e" />


UC03 — Verificar Estoque

Atores: Sistema, Atendente
Descrição: Verifica quantidade disponível do produto.
Pré-condições: Produto cadastrado no estoque.
Pós-condições: Estoque atualizado.
Fluxo Principal: Consulta estoque → Verifica quantidade → Retorna resultado.
Fluxos Alternativos: Estoque insuficiente → alerta.


**Foto do Diagrama:**


<img width="371" height="308" alt="image" src="https://github.com/user-attachments/assets/015e901b-7f05-4619-b44d-41d98b3615e8" />


UC04 — Registrar Venda

Atores: Atendente, Cliente
Descrição: Registra venda, atualiza estoque e gera comprovante.
Pré-condições: Cliente identificado, estoque disponível.
Pós-condições: Venda registrada; estoque atualizado.
Fluxo Principal: Seleciona produtos → Verifica estoque → Define quantidade/pagamento → Sistema registra → Gera comprovante.
Fluxos Alternativos: Estoque insuficiente; Cliente não cadastrado.


**Foto do Diagrama:**


<img width="492" height="506" alt="image" src="https://github.com/user-attachments/assets/2f49f5a9-b52a-4be4-8079-f799455846ba" />


UC05 — Emitir Comprovante de Venda

Ator: Atendente
Descrição: Emite comprovante da venda.
Pré-condições: Venda registrada.
Pós-condições: Comprovante entregue.
Fluxo Principal: Sistema gera → Atendente entrega.
Fluxos Alternativos: Falha na impressão/envio → alerta.


**Foto do Diagrama:**


<img width="344" height="257" alt="image" src="https://github.com/user-attachments/assets/af522057-51dc-4c2c-8c1a-7ee647198746" />


UC06 — Registrar Venda a Prazo

Atores: Atendente, Cliente
Descrição: Registra venda com pagamento futuro.
Pré-condições: Cliente cadastrado; estoque disponível.
Pós-condições: Conta a receber gerada; estoque atualizado.


**Foto do Diagrama:**


<img width="372" height="422" alt="image" src="https://github.com/user-attachments/assets/9f41ce29-2f99-43e2-a5a2-d6a349008ba3" />


UC07 — Atualizar Estoque

Atores: Sistema, Gerente
Descrição: Atualiza estoque após venda ou compra.
Pré-condições: Produto cadastrado.
Pós-condições: Estoque atualizado.


**Foto do Diagrama:**


<img width="231" height="341" alt="image" src="https://github.com/user-attachments/assets/c421a4cd-b885-4011-9c2b-718b3a8393ee" />


UC08 — Consultar Histórico de Vendas do Cliente

Atores: Atendente, Cliente
Descrição: Consulta compras anteriores de um cliente.
Pré-condições: Cliente cadastrado.
Pós-condições: Histórico exibido.


**Foto do Diagrama:**


<img width="209" height="341" alt="image" src="https://github.com/user-attachments/assets/7b1fd94a-8677-4725-905c-e84ebaf2fade" />


UC09 — Gerenciar Produtos

Ator: Gerente
Descrição: Cadastra ou edita produtos.
Pré-condições: Produto existente ou novo.
Pós-condições: Produto atualizado/cadastrado.


**Foto do Diagrama:**


<img width="197" height="396" alt="image" src="https://github.com/user-attachments/assets/368e55ec-be14-45e9-853f-cbe47879b0bb" />


UC10 — Gerar Contas a Receber

Ator: Financeiro
Descrição: Cria contas a receber para vendas a prazo.
Pré-condições: Venda a prazo registrada.
Pós-condições: Conta registrada no financeiro.


**Foto do Diagrama:**


<img width="176" height="396" alt="image" src="https://github.com/user-attachments/assets/f7a5872b-206f-4320-b848-d0741da9aabb" />

---
