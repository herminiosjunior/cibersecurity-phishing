# Cibersecurity-facebook-phishing

Este documento demonstra o processo realizado para configurar um ambiente de phishing no Kali Linux usando o SEToolkit. **Este projeto é exclusivamente educacional, visando à conscientização sobre segurança.**

---

## Ferramentas Utilizadas

- **Kali Linux**: Sistema operacional utilizado para o ambiente de testes.
- **SEToolkit**: Ferramenta escolhida para realizar a coleta de credenciais.

---

## Execução do Phishing com SEToolkit

1. **Elevação para Root**  
   Iniciado o ambiente com permissões de superusuário através do comando `sudo su`, permitindo acesso total às ferramentas necessárias.

2. **Início do SEToolkit**  
   O SEToolkit foi iniciado com o comando `setoolkit`, carregando o menu de ataques de engenharia social.

3. **Seleção do Tipo e Vetor de Ataque**  
   No menu do SEToolkit, foi selecionado o tipo de ataque de **Engenharia Social**, seguido do vetor de ataque **Web Site Attack Vectors**, que permite replicar páginas web para captura de dados.

4. **Definição do Método de Captura de Credenciais**  
   O método **Credential Harvester Attack** foi configurado com o modo **Site Cloner**, para clonar uma página específica e capturar credenciais inseridas.

5. **Configuração do IP Local e URL do Clone**  
   - **IP da Máquina**: Obtido com `ifconfig`, definindo o IP que receberia as credenciais.
   - **URL do Clone**: Foi configurado para replicar `http://www.facebook.com`, criando uma cópia visual da página.

6. **Captura de Credenciais**  
   Com o ambiente configurado, o SEToolkit aguardou que as credenciais fossem inseridas pela vítima, capturando informações como endereço IP da origem, data e hora, além das credenciais fornecidas.

---

## Resultados Obtidos

Os dados capturados foram exibidos no terminal conforme imagem abaixo, onde o SEToolkit estava rodando, incluindo:

- Endereço IP da vítima
- Data e hora de acesso
- Credenciais submetidas (caso presentes)

---

**Aviso Legal:** A prática de phishing sem autorização é ilegal. Este projeto serve exclusivamente para conscientização e fins educacionais, abordando a importância de medidas preventivas em segurança cibernética.

---

Esta documentação reflete a execução prática do SEToolkit para fins de aprendizado e teste seguro em ambientes controlados.
