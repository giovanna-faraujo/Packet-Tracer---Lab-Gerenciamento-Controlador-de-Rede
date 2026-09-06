# Implementação e Monitoramento de Redes com Controlador Centralizado (SDN) no Cisco Packet Tracer

**Resumo Rápido:** Instalação física e integração de um Network Controller corporativo em ambiente simulado para gerenciamento centralizado, descoberta automatizada de topologia e telemetria de clientes em tempo real.

---

## 1. O que é este projeto? (Explicado de forma simples)
Pense em uma grande torre de controle de tráfego aéreo em um aeroporto internacional. Em vez de cada piloto precisar adivinhar onde estão os outros aviões ou conversar individualmente com cada pista pelo rádio, os operadores olham para uma tela única com radares em tempo real: eles sabem quem decolou, quem pousou, quais aeronaves estão se aproximando e qual pista está livre.

Em redes tradicionais de computadores, o técnico precisava entrar aparelho por aparelho (switch por switch, roteador por roteador) digitando comandos para descobrir quem estava conectado. Com um Controlador de Rede (conceito moderno chamado de Redes Definidas por Software ou SDN), instalamos um equipamento que atua exatamente como essa torre de controle. Acessando uma página web amigável pelo navegador, o administrador de rede enxerga toda a topologia corporativa, identifica automaticamente novos celulares e tablets que entram no Wi-Fi e acompanha a saúde da infraestrutura de ponta a ponta sem intervenções manuais repetitivas.

---

## 2. Objetivo e Valor para o Negócio
- **Problema Enfrentado:** Dificuldade em manter o inventário de ativos atualizado e lentidão para identificar novos dispositivos móveis que se conectam à rede corporativa por meio de auditorias manuais, gerando riscos de segurança por falta de visibilidade.
- **Solução Aplicada:** Implementação física de um Network Controller conectado ao switch corporativo, integrando serviços de descoberta automatizada (Discovery) e rastreamento de hosts (Assurance) através de interface gráfica web.
- **Impacto Prático:** Visibilidade em tempo real de 100% dos ativos conectados em painel único, redução do tempo de suporte e eliminação de pontos cegos de segurança na rede local.

---

## 3. Tecnologias e Competências Praticadas
- **Ambiente e Ferramentas:** Cisco Packet Tracer (Ambiente Lógico e Wiring Closet), Cisco Network Controller, Switch Corporativo Office-SW1 (Catalyst), Terminal de Gestão (Office-Admin), Tablet e Smartphone.
- **Técnicas e Metodologias:** Redes Definidas por Software (SDN Architecture), Descoberta Automatizada de Topologia (Network Discovery), Telemetria de Conectividade (Host Assurance), Endereçamento IPv4 Dinâmico (DHCP) e Cabeamento Estruturado em Rack.
- **Competências Profissionais Evidenciadas:** Governança de ativos de TI, monitoramento proativo de infraestrutura, resolução metódica de incidentes de rede e operação de dashboards de controle corporativo.

---

<img width="1041" height="910" alt="image" src="https://github.com/user-attachments/assets/b19b506b-1bbc-450a-bb3e-ea58f9077647" />

---


<img width="311" height="312" alt="image" src="https://github.com/user-attachments/assets/2b0ef99b-d356-4ebe-b90e-19b9e61af4f6" />

---

<img width="635" height="370" alt="image" src="https://github.com/user-attachments/assets/82194160-6eba-4787-8fbb-33523af94fb8" />

---

#

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
