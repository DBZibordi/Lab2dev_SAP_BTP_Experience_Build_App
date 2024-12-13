# Adicione mais funcionalidades à sua aplicação

## Introdução

Nesta seção você irá criar uma página para mostrar os detalhes do parceiro de negócios selecionado para sua aplicação.

## Pré-requisitos:

- Você deve ter completado os exercícios anteriores
- Sua aplicação SAP Build deve estar funcionando e a página de lista deve carregar

## Passo 1: Criando uma nova página

Você adicionará uma nova página à sua aplicação e adicionará parâmetros de página para que você possa acessar dados de sua aplicação.

1. Na aba **User Interface**, clique no campo com o nome da sua página atual **Home** e depois eo **Add new page**.

    <p align="center"><img src="./images/ex2_part1_1.png" width="100%" /></p>

2. No pop-up que abrirá, preencha o nome da página com `Details`e então clique no botão **OK**.*. Sua nova página será criada e aberta.

3. Em seguinda, na aba **VARIABLES**, selecione a opção **PAGE PARAMETERS** no lado esquerdo da tela e clique no botão **ADD PARAMETER**.

    <p align="center"><img src="./images/ex2_part1_2.png" width="100%" /></p>

4. Criar um novo parâmetro, selecione o parâmetro criado para editar.

5. No lado direito da tela, altere o **Variable name** para `businessPartnerId`.

6. Novamente, escolha **ADD PARAMETER**. e crie um segundo parâmetro.

7. Alterar nome do parâmetro para `businessPartnerName`.

8. Por último clique em **SAVE**.

## Passo 2: Habilitar a navegação da Home Page para a Detail Page

Para exibir os detalhes do parceiro de negócios na página de detalhes, você precisa conectar a página **Home** e a página **Details**. Nesta seção, você primeiro criará uma nova lógica de navegação para passar o parâmetro da página criado na etapa anterior. Na página de detalhes, você carregará o endereço do parceiro de negócios passando o id do parceiro de negócios para a entidade **BusinessPartners**.

1. Na aba **User Interface** mude da página atual **Details** para a página **Home**.

2. Na página **Home**, selecione a primeira linha da lista que havíamos criado

4. Na parte inferior do App Builder, onde você pode ver **Add logic to LIST ITEM1**. Escolha a seta para abrir o canvas de lógica.

    <p align="center"><img src="./images/ex2_part2_1.png" width="100%" /></p>

5. No menu de componentes no lado esquerdo, escolha **NAVIGATION → Open page** para adicionar uma função que navega para uma nova página.

6. Arraste e solte para a tela de lógica.

7. Passe o mouse sobre o **Component tap** e clique sobre o ponto redondo. Conecte os pontos dos componentes **Component tap** e **Open page**. Isso cria uma nova conexão e define a lógica para abrir uma nova página no evento de toque em um item na lista.

    <p align="center"><img src="./images/ex2_part2_2.png" width="100%" /></p>

8. Selecione o componente **Open page**.

9. No lado direito da tela, selecione **PROPERTIES → Parameters → businessPartnerId**.

10. Selecione o botão **X**. Irá abrir um popup.

    <p align="center"><img src="./images/ex2_part2_3.png" width="100%" /></p>

11. Selecione **Data item in repeat**.

12. Selecione **current**.

13. Role a lista e selecione **BussinessPartner**, e então clique em **SAVE**.

14. Repita o mesmo para o parâmetro **businesspartnerName** e selecione **BusinessPartnerFullName**.

<p align="center"><img src="./images/ex2_part2_4.png" width="100%" /></p>

15. Clique no botão **SAVE** para salvar as alterações.

Neste passo, você pode passar o código do parceiro de negócios selecionado para navegar para a página de detalhes.

## Passo 3: Carregar os dados de um parceiro de negócios na página de detalhes

A página de detalhes recebe o código do parceiro de negócios da página principal. Com essa informação é possível obter demais dados de um parceiro de negócios selecionado das demais entidades que habilitamos.

1. Na aba **Variables** selecione a página **Details** para mudar para a página de detalhes.

4. Selecione a opção **DATA VARIABLES** no lado esquerdo da tela.

5. Clique na opção **ADD DATA VARIABLE**.

6. Selecione **A_BusinessPartnerAddress** da lista.

7. Defina o **Data variable name** para `BusinessPartnerAddress`.

8. Selecione o botão **Filter Conditions** no lado direito.

    <p align="center"><img src="./images/ex2_part3_1.png" width="100%" /></p>

9. Um popup será aberto. Selecione **Object with properties**.

    <p align="center"><img src="./images/ex2_part3_2.png" width="60%" /></p>

10. Selecione a opção **Add Condition**. No dropdown **Property**, selecione **BusinessPartner** e sob a propriedade **Compared Value**, clique no botão **ABC**.

    <p align="center"><img src="./images/ex2_part3_3.png" width="100%" /></p>

11. Selecione **Data and Variables**.

    <p align="center"><img src="./images/ex2_part3_4.png" width="100%" /></p>

12. Selecione **Page parameter**.

    <p align="center"><img src="./images/ex2_part3_5.png" width="100%" /></p>

13. Selecione **businessPartnerId** em clique no botão salvar **SAVE**.

    <p align="center"><img src="./images/ex2_part3_6.png" width="100%" /></p>

14. Clique no botão **SAVE** para salvar as alterações na página.

15. Mude para o modo **VIEW**.

Agora, sua aplicação carrega os dados de um parceiro de negócios selecionado e armazena na variável de dados.

## Passo 4: Exibir o ID do parceiro de negócios na página de detalhes

Você irá alterar o cabeçalho da página de detalhes, para que ele exiba o parceiro de negócios atual.

1. Na aba **User Interface**, na página **Details**, selecione o componente **Title** e arraste para a página. No lado direito da tela, clique no botão **ABC** na seção **Content**.

    <p align="center"><img src="./images/ex2_part4_1.png" width="100%" /></p>

3. Selecione **Data and Variables**.

    <p align="center"><img src="./images/ex2_part4_3.png" width="80%" /></p>

4. Selecione **Page parameter**.

    <p align="center"><img src="./images/ex2_part4_4.png" width="80%" /></p>

5. Selecione **businessPartnerName** e escreva `Nome do Parceiro de Negócio` no campo **Optional preview value**.

6. Clique no botão **SAVE**.

    <p align="center"><img src="./images/ex2_part4_5.png" width="100%" /></p>

## Passo 5: Exibir as informações do parceiro de negócios na página de detalhes

1. Arraste para a página um **Container** da aba **CORE** à esquerda para a tela.

2. No lado direito em **PROPERTIES**, clique no botão **Repeat with**.

    <p align="center"><img src="./images/ex2_part5_1.png" width="100%" /></p>

3. No popup, selecione **Data and Variables → Data variable**.

4. Selecione **BusinessPartnerAddress** na lista.

5. E clique em **SAVE**.

    <p align="center"><img src="./images/ex2_part5_2.png" width="100%" /></p>

6. Agora, arraste um componente **Row** para dentro do container criado.

    <p align="center"><img src="./images/ex2_part5_2_1.png" width="100%" /></p>

7. Arraste um componente **Text** da aba **CORE** para o lado esquerdo do componente **Row**.

8. No lado direito em **PROPERTIES**, clique no botão **ABC** em **Content**

   <p align="center"><img src="./images/ex2_part5_2_2.png" width="100%" /></p>

9. Selecione **Formula**, depois, no menu lateral, escolha **Currently repeated data items**, procure na lista por **repeated.current.StreetName** e clique em **Enter +**. Por fim, clique em salvar **SAVE**

   <p align="center"><img src="./images/ex2_part5_2_3.png" width="100%" /></p>

10. No lado direito da tela, no campo **Content** preencha o campo com Nome do Parceiro.

    <p align="center"><img src="./images/ex2_part5_3.png" width="100%" /></p>

11. Arraste um componente **Text** da aba **CORE** para o lado direito do componente **Row**.

12. No lado direito da tela, clique no botão **ABC** na seção **Content**.

    <p align="center"><img src="./images/ex2_part5_4.png" width="100%" /></p>

13. Selecione **Data item in repeat**.

14. No campo select repeat selecione  **current**, no campo select repeat data property selecione **partnerName** e por último no campo Set preview value escreva Parceiro.

    <p align="center"><img src="./images/ex2_part5_5.png" width="100%" /></p>

15. Clique em **SAVE**.

16. Repita os passos anteriores para os seguintes campos:

    |Field name | Field type |
    |----|----|
    |Email | Text |
    |Address | Text |
    |Phone | Text |

    <p align="center"><img src="./images/ex2_part5_6.png" width="100%" /></p>

17. Clique no botão **SAVE** para salvar as alterações na página.


## Passo 6: Pré visualização da aplicação

1. Clique na aba **LAUNCH**.

2. Selecione a opção **OPEN PREVIEW PORTAL** e depois clique no botão **Open web preview**.

3. Selecione sua aplicação.

    <p align="center"><img src="./images/ex2_part6_1.png" width="70%" /></p>

A home page deve ser parecida com a imagem abaixo:

<p align="center"><img src="./images/ex2_part6_3.png" width="100%" /></p>

A página de detalhes deve ser parecida com a imagem abaixo:

<p align="center"><img src="./images/ex2_part6_4.png" width="100%" /></p>


## Passo 7: Adicionando opção de chamada

1. Ná página de detalhes, arraste um componente **Button** da aba **CORE** para o canvas, preencha o campo label com o valor `Ligar para o Parceiro de Negócios` e por último selecione o campo abaixo para adicionar uma lógica ao botão.

    <p align="center"><img src="./images/ex2_part7_1.png" width="100%" /></p>

2. Clique em **MARKETPLACE**.

    <p align="center"><img src="./images/ex2_part7_2.png" width="70%" /></p>

3. Procure por **Open URL** e clique no resultado destacado abaixo.

    <p align="center"><img src="./images/ex2_part7_3.png" width="100%" /></p>

4. Clique no botão **Install**.

5. Arraste o **Open URL** para o canvas.

6. Conecte os dois **Componentes** passando o mouse sobre os pontos finais e conectando-os.

    <p align="center"><img src="./images/ex2_part7_4.png" width="100%" /></p>

7. Clique no botão **Open URL** e pressione o botão **ABC**.

    <p align="center"><img src="./images/ex2_part7_5.png" width="100%" /></p>

8. Clique em **Formula**.

9. E escreva a seguinte expressão `""tel:"+data.Business_Partners[0].phone`.

    <p align="center"><img src="./images/ex2_part7_6.png" width="100%" /></p>

10. Clique em **Save**.

11. Parabéns, você adicionou a função de **Ligar** para o seu aplicativo e pode testar no **Web Preview**.

## Parabéns

Incrível! Você completou o Exercício 2. 🥳

Você pode voltar para a página Overview [Overview](../../#exercises).  
Ou você pode seguir para o próximo exercício [Exercise 3](../ex3/), navegue para lá clicando no link [this link](../ex3/).

