# Laboratório: Monitoramento e Gerenciamento com Controlador de Rede (SDN)

## O que é este projeto? (Explicação Simples)

Gerenciar uma rede de computadores de forma individual pode ser demorado e complexo. O **Controlador de Rede** funciona como uma "torre de controle" ou um painel centralizado: em vez de configurar aparelho por aparelho, o administrador consegue visualizar, gerenciar e proteger toda a infraestrutura através de uma única tela no navegador.

Neste laboratório, foi implantado um controlador central para identificar automaticamente os equipamentos da rede e monitorar a entrada de novos dispositivos sem fio (como tablets e smartphones).

<img width="1041" height="910" alt="image" src="https://github.com/user-attachments/assets/b19b506b-1bbc-450a-bb3e-ea58f9077647" />

---

## Objetivos Técnicos
- Conectar e energizar o Controlador de Rede no rack principal.
- Validar a conectividade de Camada 3 via ICMP (`ping`).
- Acessar a interface gráfica (GUI) do controlador via navegador web.
- Executar o processo de **Network Discovery** para identificar novos hosts na rede.
- Documentar a topologia e o endereçamento IP da infraestrutura.

<img width="311" height="312" alt="image" src="https://github.com/user-attachments/assets/2b0ef99b-d356-4ebe-b90e-19b9e61af4f6" />

---

<img width="635" height="370" alt="image" src="https://github.com/user-attachments/assets/82194160-6eba-4787-8fbb-33523af94fb8" />

---

## Passo a Passo Realizado

### Parte 1: Implementação e Conectividade Física
1. No Armário de Cabeamento (*Wiring Closet*), o **Network Controller** foi movido do estante (*Shelf*) para o *Rack*.
2. Conectou-se a interface `GigabitEthernet0` do controlador à porta `GigabitEthernet 1/0/19` do switch `Office-SW1` utilizando um cable directo (*Copper Straight-Through*).
3. A partir do computador `Office-Admin`, verificou-se o endereço IP obtido via DHCP (`192.168.20.x`) e testou-se a comunicação com o controlador (`192.168.20.5`).

---

### Parte 2: Acesso ao Painel Central (GUI)
1. Através do navegador em `Office-Admin`, realizou-se o acesso ao endereço `192.168.20.5` com as credenciais administrativas.
2. Exploração das seções do menu principal:
   - **Dashboard:** Visão geral do estado de saúde da rede.
   - **Provisioning:** Gerenciamento e descoberta de ativos (*Network Device* e *Discovery*).
   - **Assurance:** Monitoramento e métricas de desempenho dos *Hosts*.
   - **Policy:** Configuração de políticas e regras da rede.

---

### Parte 3: Descoberta de Novos Dispositivos (Discovery)
1. Na aba **Assurance > HOSTS**, listou-se os dispositivos inicialmente conectados.
2. Os dispositivos `Office-Tablet` e `Smartphone` foram ligados e associados à rede sem fio (`Wireless0`), recebendo endereços IP via DHCP no segmento `192.168.2.0/24`.
3. Na aba **Provisioning > DISCOVERY**, executou-se a tarefa de busca **Office LAN**.
4. O controlador identificou com sucesso os novos dispositivos sem fio e atualizou a lista de hosts monitorados.

<img width="680" height="467" alt="image" src="https://github.com/user-attachments/assets/455cf080-d12e-4785-998a-98ee685dafcb" />
---
<img width="1038" height="664" alt="image" src="https://github.com/user-attachments/assets/654182de-eb5d-4f18-a345-cc23772f41fc" />


---

## Resumo dos Endereços da Rede

| Dispositivo | Interface / Papel | Endereço IP / Sub-rede |
| :--- | :--- | :--- |
| **Network Controller** | GigabitEthernet0 | `192.168.20.5` |
| **Office-SW1** | Switch de Acesso | `192.168.20.4` |
| **Office-Admin** | Estação de Gerenciamento | `192.168.20.x /25` (DHCP) |
| **Dispositivos Sem Fio** | Office-Tablet / Smartphone | `192.168.2.x /24` (DHCP) |

<img width="1907" height="950" alt="image" src="https://github.com/user-attachments/assets/3bb73028-6785-42e0-8569-29a948007774" />

---

> 📝 **Nota de Autoria:**  
> *Este exercício é baseado no material prático original da **Cisco Networking Academy (NetAcad)** realizado no software **Cisco Packet Tracer**, documentado e estruturado para fins educacionais e de demonstração de conhecimento técnico.*
