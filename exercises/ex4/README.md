# Integre seu aplicativo com o SAP Build Work Zone, standard edition.

## Introdução

Nesta seção, o aplicativo será conectado com o SAP Build Work Zone, standard edition. Isso permite ter um ponto de entrada central para utilizar os aplicativos no SAP BTP.

## Pré-requisitos

- Concluiu os exercícios anteriores
- Seu SAP Build App foi criado com sucesso

## Etapa 1: Integre seu aplicativo com SAP Build Work Zone, standard edition

1. Na sua Subaccount, abra o menu lateral **Services**, depois escolha **Instances and Subscriptions** e abra o **SAP Build Work Zone, standard edition**
   
    <p align="center"><img src="./images/1.png" width="100%" /></p>   

2. Na tela que foi aberta, no menu do lado esquerdo, escolha o ícone do **Gerenciador de canais** e depois clique no ícone de atualização para buscar o conteúdo atualizado.

    <p align="center"><img src="./images/2.png" width="100%" /></p>   

3. No menu lateral escolha **Gerenciador de conteúdo** e depois em  **Explorador de conteúdo**.
   
    <p align="center"><img src="./images/3.png" width="100%" /></p>   

4. Selecione o bloco **HTML5 Apps** do seu respectivo de subdomínio.

    <p align="center"><img src="./images/4.png" width="100%" /></p>   

5. Procure pelo aplicativo com o nome criado no Build Apps `BTP_EXP_01`, marque a caixa de seleção e selecione o botão **Adicionar** .

    <p align="center"><img src="./images/5.png" width="100%" /></p>   

6. No menu lateral abra novamente o **Gerenciador de conteúdo**, clique no botão **Criar** e selecione **Grupo** no menu suspenso.
   
    <p align="center"><img src="./images/6.png" width="100%" /></p>   

7. Insira o nome do grupo `Apps do XP161_01`, procure pelo aplicativo `BTP_EXP_01` que foi adicionado anteriormente no Gerenciador de Conteúdo, mude o campo **Status de Atribuição** conforme abaixo e clique em **Salvar**:

    <p align="center"><img src="./images/7.png" width="100%" /></p>   

8. No menu lateral abra novamente o **Gerenciador de conteúdo**, clique no botão **Criar** e selecione **Função** no menu suspenso.

    <p align="center"><img src="./images/8.png" width="100%" /></p>   

9. Insira o nome da função `XP161_01`, procure pelo aplicativo `BTP_EXP_01` que foi adicionado anteriormente no Gerenciador de Conteúdo, mude o campo **Status de Atribuição** conforme abaixo e clique em **Salvar**:

    <p align="center"><img src="./images/9.png" width="100%" /></p>   

10. No menu do lado esquerdo navegue até **Diretório de Sites** e no bloco clique no botão **+ Criar site**

    <p align="center"><img src="./images/10.png" width="100%" /></p>   

11. Preencha o campo Nome do site do pop-up com `XP161_01` e clique em  **Criar**

    <p align="center"><img src="./images/11.png" width="100%" /></p>    

12. Agora, você será encaminhado para o editor do site. Clique em **Editar**, procure a função `XP161_01` na coluna da direita, clique no botão **+** e depois em **Salvar**

    <p align="center"><img src="./images/12.png" width="100%" /></p>    
    
...

25. Go back to the Site Directory and find your created site. Open it by choosing the small **Go to site** icon.

    <p align="center"><img src="./images/9 site_directory.png" width="100%" /></p>

26. You should be able to see your app in its defined section

    <p align="center"><img src="./images/10 site.png" width="100%" /></p>

## Step 2: Use your app in SAP Mobile Start

1. On your Site and select **Settings** from your **profile icon**

    <p align="center"><img src="./images/WZ_1.png" width="100%" /></p>

2. Go to **SAP Mobile Start** in the settings and select your **platform** and the **Register tab**

    <p align="center"><img src="./images/WZ_2.png" width="100%" /></p>

4. Open your SAP Mobile Start app, **agree** to the EULA and Privacy statements and **scan** the QR-Code

    <p align="center"><img src="./images/SMS_1.PNG" width="45%" /></p>
    <p align="center"><img src="./images/SMS_2.PNG" width="45%" /></p>

5. Enter your user credentials to login

    <p align="center"><img src="./images/SMS_4 placeholder login.PNG" width="45%" /></p>

6. Find and open your app in SAP Mobile Start

    <p align="center"><img src="./images/SMS_5.png" width="45%" /></p>
    <p align="center"><img src="./images/SMS_6.png" width="45%" /></p>

## Congrats

You Rock! You completed Exercise 4. 🥳

Congratulations! You now have finished the development of your application. In this last step you have integrated your app in SAP Build Work Zone, standard edition, to have one central entry point to show all of your SAP BTP applications. Finally, you have have opend your app in SAP Mobile Start.

You can now navigate to the [Overview](../../#exercises).  
