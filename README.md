## **Projeto Individual - Date Analytics**
_Projeto Individual do Módulo 02 - Programadores Cariocas 2024_

<br><br>

# **_Sistema RESILIADATA_**

## _PROPOSTA DO TRABALHO: <br>_
Você foi contratado para desenvolver um banco de dados que irá armazenar dados
importantes que será utilizado pelo sistema RESILIADATA.
  + O sistema irá auxiliar na avaliação de quais são as tecnologias que as empresas parceiras
estão utilizando e quem são seus colaboradores; <br>
  + Vamos ter o cadastro de empresas parceiras, cadastro de tecnologias com a opção de
selecionar a área (webdev, dados, marketing, etc.), uma tabela para registrar quais
tecnologias as empresas estão utilizando e uma tabela para cadastro de colaboradores.
<br><br><br>


## _PERGUNTAS: <br>_
**1. Quais são as entidades necessárias? <br>**
   Empresa Parceira, Tecnologia e Colaborador
<br><br><br>

   
**2. Quais são os principais campos e seus respectivos tipos?**
   * ***Empresa Parceira:***
     * ID (int - Inteiro, chave primária)
     * Nome (varchar - String/Texto de tamanho variável com limite)
     * CNPJ (varchar - String/Texto de tamanho variável com limite, para que caso tenho um 0 a esquerda, não seja ignorado)
     * Endereço (varchar - String/Texto de tamanho variável com limite)
     * Telefone (varchar - String/Texto de tamanho variável com limite, para que caso tenho um 0 a esquerda, não seja ignorado)
       <br><br>
     
   * ***Tecnologia:***
     * ID (int - Inteiro, chave primária)
     * Nome (varchar - String/Texto de tamanho variável com limite)
     * Área (varchar - String/Texto de tamanho variável com limite)
       <br><br>
     
   * ***Colaborador:***
     * ID (int - Inteiro, chave primária)
     * Nome (varchar - String/Texto de tamanho variável com limite)
     * CPF (varchar - String/Texto de tamanho variável com limite, para que caso tenho um 0 a esquerda, não seja ignorado)
     * Cargo (varchar - String/Texto de tamanho variável com limite)
     * Telefone (varchar - String/Texto de tamanho variável com limite, para que caso tenho um 0 a esquerda, não seja ignorado)
     * ID_Empresa Parceira (int - Inteiro, chave estrangeira referenciando a tabela Empresa Parceira)
     * ID_Tecnologia (int - Inteiro, chave estrangeira referenciando a tabela Tecnologia)
<br><br><br>


**3. Como essas entidades estão relacionadas?**
   * _Empresa Parceira - Tecnologia = 1:N <br>_
     Uma Empresa Parceira pode estar associada a várias Tecnologias, portanto é uma relação de "uma para muitas".
     
   * _Colaborador - Tecnologia = N:N <br>_
     Apesar de um Colaborador só poder estar associado a uma Empresa Parceira, ele pode possuir conhecimento em várias Tecnologias. Esse é um relacionamento de "muitos para muitos", onde múltiplos colaboradores podem ter conhecimento em múltiplas tecnologias.
     
   * _Empresa Parceira - Colaborador = 1:N <br>_
     Um Colaborador pode estar associado a/trabalha para apenas uma Empresa Parceira. Esse é um relacionamento de "uma para muitos", onde uma empresa pode ter vários colaboradores, mas um colaborador está associado a apenas uma empresa.
<br><br>

![image](https://github.com/Larifabrahao/projeto_individual_dados_mod2/assets/113908290/a1fe07d4-2b0c-4100-8eb8-cbf3df08b390)
<br><br><br>


**4. Simule 2 registros para cada entidade. <br><br>**
![image](https://github.com/Larifabrahao/projeto_individual_dados_mod2/assets/113908290/e5d1ad77-507e-4a65-9fc9-173127ecc848)

<br>

**EMPRESA PARCEIRA**

|         ID     |      Nome      |      CNPJ      |      Endereço      |      Telefone      |
| :------------------------------: | :----------------: | :----------------: | :----------------: | :----------------: |
|        01         |    Tecno AS    |    73.487.130/0001-74   |    Rua Rubens Della Volpe, 475, Cittá Di Firenze, Campinas - SP    |    (19) 3852-0285    |
|        02         |    Loudersx TEC LTDA    |    84.912.086/0001-19   |    Rua Sena Madureira, 115, Conjunto Bela Vista, Rio Branco - AC    |      (11) 3735-6936      |


**<br><br> TECNOLOGIA**

|      ID      |      Nome      |      Área      |
| :--------------------------: | :----------------: | :----------------: |
|      01       |  Python  |  Webdev |
|      02       |  MySQL  |  Dados |


**<br><br> COLABORADOR**

|         ID        |      Nome      |      CPF      |      Cargo      |      Telefone      |      ID_Tecnologia      |      ID_Empresa Parceira      |
| :------------------------------: | :----------------: | :----------------: | :----------------: | :----------------: | :----------------: | :----------------: |
|        01         |    Otávio Enzo Alexandre Gonçalves    |    444.384.272-15   |    Desenvolvedor Júnior    |    (91) 99902-5416    |    02   |    01    |
|        02         |    Augusto Vitor Yuri Aparício    |    429.178.530-50   |    Desenvolvedor Sênior    |    (82) 98900-6826    |    01   |    02    |

<br><br><br>



