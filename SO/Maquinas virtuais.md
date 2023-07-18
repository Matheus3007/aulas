- Software para simular o comportamento de máquinas físicas em cima de hardware.
- Utilizadas para executar aplicações legado em SO em hardware atual
- Segurança
	- Isolamento e containerização dos dispositivos
	- Proteção de dados

## Principio de funcionamento
- Usando os serviços oferecidos por uma determinada interface de sistema a camada de virtualização constrói outra interface de mesmo nível
- A camada de virtualização é denominada hipervisor
	- Monitor de maquina virtual VMM
- Nova interface do sistema
-
## Componentes
- [[O sistema real]] (host)
	- Contém recursos reais de hardware
- Camada de virtualização ([[Hypervisor]])
	- Constrói a interface virtual a apartir da interface real
- [[Sistema virtual]] (guest)
	- Executa sobre a camada de virtualização