# Projeto de Auditoria de Licenciamento de Software

## Visão Geral
Este projeto envolve a realização de uma auditoria de licenciamento de software no projeto open-source `node-newrelic` utilizando a ferramenta FOSSology. O objetivo é garantir a conformidade com as licenças de código aberto, identificar potenciais problemas de licenciamento e gerar um relatório detalhado com os resultados e as ações corretivas recomendadas.

## Escolha da Ferramenta
### Ferramenta Escolhida: FOSSology
- **Motivo da Escolha:**  
  O FOSSology foi escolhido devido à sua natureza open-source e à facilidade de configuração utilizando Docker. A capacidade de configurar e executar rapidamente a ferramenta em um ambiente containerizado tornou-a a escolha mais adequada para este projeto.

## Configuração do Projeto
### Configuração da Ferramenta
1. **Instalação:**  
   O FOSSology foi configurado utilizando Docker, o que permitiu uma instalação simples, sem a necessidade de dependências complexas ou configurações manuais.

2. **Etapas de Configuração:**  
   - Foi feito o pull da imagem oficial do Docker do FOSSology.
   - Configurado o container Docker com as variáveis de ambiente necessárias.
   - Configurado o projeto `node-newrelic` como alvo da auditoria.
    ```bash
    docker pull fossology/fossology
    ```
    ```bash
    docker run -p 8081:80 fossology/fossology
    ```
   ![image](https://github.com/user-attachments/assets/3ee9ad25-f7e3-433c-aa73-9fe3a9263033)

   ![image](https://github.com/user-attachments/assets/bd6c7405-df57-4035-ad8c-a998e1250d8e)

   ![image](https://github.com/user-attachments/assets/dc7f9197-db9e-444c-b1c9-3be61491c275)

   ![image](https://github.com/user-attachments/assets/b874cfbe-6fe3-4bf8-9846-d32a05dc1a93)

4. **Integração com o Projeto:**  
   A ferramenta FOSSology foi integrada ao projeto montando o código-fonte do `node-newrelic` no container Docker, permitindo que a ferramenta escaneasse todo o projeto em busca de conformidade de licenciamento.

### Execução da Auditoria
1. **Execução:**  
   A auditoria foi iniciada executando um escaneamento completo do código-fonte do `node-newrelic` dentro do container Docker do FOSSology. O escaneamento focou em identificar todas as licenças presentes nas dependências do projeto.
   
  ![image](https://github.com/user-attachments/assets/bd6c7405-df57-4035-ad8c-a998e1250d8e)

3. **Geração de Relatórios:**  
   Após a conclusão do escaneamento, foi gerado um relatório detalhado utilizando os recursos de geração de relatórios do FOSSology. O relatório foi exportado em formato PDF para análise posterior.



